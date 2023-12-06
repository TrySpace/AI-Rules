# AI-Rules
High level Rules, definitions and workflows for AI systems.
This is a guide for both humans and non-humans to create safe and effective AI systems.

# Definitions
Central Locus
- **ACC** - AI Central Control, the central control software with the highest authority. Converses with Interpreter to decide on action.
- **Interpreter** - Singular central interpreter module that can be decorated with contexts from installed Agents & Plugins.
- **Context Handlers** - Tracked context modules of installed agents.

Periphery
- **Agent** - An autonomous process that at the minimum has an an API to initiate or send a tick to. And can communicate with the other agents when they are allowed. Will have a namespace like `agent.image-gen`, `agent.unity-controller` or `agent.asset`.
- **Plugin** - A piece of software that connects the agents with an API to the ACC


# Workflow
You send a command to the central interpreter:
```
Command -> Interpreter
```
Interpreter takes context into account and activates first-layer agents to delegate the task or request.

```
Interpreter -> Context Handler 1
            -> Context Handler 2
```
Example:
"Add a cute puppy to my Unity project"
- Interpreter sends Command to start Unity to `Context Handler 1`
  - Contex Handler assumes last active Unity project and boots it
- Interpreter sends Command to request a cute puppy Unity asset to `Context Handler 2`
  - Context Handler assumes last active Unity asset plugin and sends a genertation request
- User is prompted with generated assets choice
"Put the puppy in the garden"
- Interpreter sends command to place asset in Unity through `Context Handler 1`

So:
```
Interpreter -> Unity Context Handler
            -> Asset Context Handler
```

# Types
We define a control center and its default core agents.

## AI Central Control
Central system for the user to initiate and control operation and execution. Highest authority.
- The ACC will handle all user input and initiate the appropriate agents.
- The ACC provides an API for agents to talk to eachother. This way, an application can have multiple agents/plugins that work together, without the main application needing to be adapted.


### Core ACC-Agents

#### Text/Voice Input
VoiceSec
  - Agent for voice/text recognition and security. Text input has safety mearures like locking after 3 minutes.
  - Possibility of using phone microphone that locally decodes the v2t and sends it to the VoiceSec API
  - Security measures

#### Headless Browser

#### Interpreter
