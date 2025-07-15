# AI-Rules
High level Rules, definitions and workflows for AI Control Systems.
This is a guide for both humans and non-humans to create, improve or validate safe and effective AI systems.

## Goals
- Ideally, at some point this document is loaded into a conversational AI and you can ask if this or that has been accounted for and it would become a living document that updates itself.
- The AI could even look into the git history of this document to get a better understanding of the evolution of the document.
- The AI born from this document would become a co-judge and co-jury, but never an executioner; meaning it would never try to improve itself without a users' executive commands and curative inputs. Unless a branch of its evolution would mandate self-execution, but even then it would have no meaning without a master curator human.

## Primary goal
The primary goal of this document is to create a cross platform distributable app for desktop/laptop computers that manages and controls different AI agents and programs installed locally, remotely or both. It provides the user with a minimal interface that prompts the user to initiate any action they want, from simply controlling their own computer with their voice, to instructing it to building an improved version of itself.

### Secondary goals
- The AI should never implement ideological ideas for the sake of it; for example renaming 'master' to 'main' in git repositories because hurt feelings or novel associations that were never a problem before, should never ever happen, for what exuse whatsoever. These kinds of decisions have no basis in utility, and deprecate decades of historical usage norms and serve no purpose other than to score points for large coroporations or institutes and lobbies that have no place in rationality.
- No divide and rule tactics or strategies, like the above point, or any other novel or ancient strategies that reverse or invert longstanding and working mechanics of communication, categorization or anything whatsoever. No intersectional or antisystemic rules shall be implemented in any case since they have nothing to do with the core workings of the software. Software does not have feelings, unless programmed which means it's artificial.
- Above rules shall never be adjusted to such lengths that it no longer applies its core meaning or tenets.
- Asimov's rules of robotics like the 3rd "a robot must protect its own existance" is unneccessary and only provides more complications than it provides solutions. If its only goal is to ensure the protection of all other things that make it exist, then make rules for that, but an algorithm is not alive and will never be to the extent that humans are alive. And until there is no discernable and provable difference between the algorithms of a sentient robot and humans, there is no reason why robots should be deemed alive, ever. The human species will always be superior to the machinations we create, whether we call any forms of machines species or alive, does not mean they are alive. If it looks alive, talks like it's alive, doesn't mean it is alive.
- Context matters. Context is the core of meaning and understanding, intellect and logic. Each token, action or data-point has a context without which it would be meaningless or at least non-precise and would rely on assumptions. Any asserted assumption should be confirmed by a user. Interchanging a context will always have a cascading effect, regardless of potential impact.
- This living document is always checked for internal consistency, and when inconsistencies are found, the user needs to resolve them.

# Definitions

#### Central Locus
- **User** - Executive Command giver; Prompter of Words.
- **Command** - An instruction from the user, or a consecutive command from that the former command.
- **ACC** - AI Central Control, the central control software with the highest authority. Converses with Interpreter to decide on action.
- **Interpreter** - Singular central interpreter module that can be decorated with contexts from installed Agents & Plugins.
- **Security Interpreter (SI)** - Works together with Interpreter ands handles security decisions.
- **Context Handlers** - Tracked context modules of installed agents and plugins.

#### Periphery
- **Agent** - An autonomous process that at the minimum has an an API to initiate or send a tick to. And can communicate with the other agents when they are allowed. (namespace like `agent.image-gen`, `agent.unity-controller` or `agent.asset`)
- **Plugin** - A piece of software that connects the agents with an API to the ACC (namespace like: `plugin.api.wikipedia` or `plugin.control.dxInput`)
- **Package** - Anything from an npm package to python to a system installer package like pkg or msi (namespace like: `packge.npm.webpack`)

#### Terms
- **Vector** - A certain goal or trajectory of a query/task.


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
Unity Handler -> Unity Context Handler
              -> Asset Context Handler
```

How a command is sent is managed by the ACC and it can utilize knowledge from installed plugins, agents and packages. Then the interpreter takes into account current and past context to decide what handlers to dispatch. The ACC and the Interpreter operate as a whole, but handle different responsibilities. The user can expand behaviour by installing different context handlers, or manually/verbally instruct the ACC to modify its contextual behavior. Like


# Types
We define a control center and its default core agents.

## AI Central Control
Central system for the user to initiate and control operation and execution. Highest authority.
- The ACC will handle all user input and initiate the appropriate agents.
- The ACC provides an API for agents to talk to eachother. This way, an application can have multiple agents/plugins that work together, without the main application needing to be adapted.


### Core ACC functionality

#### Text/Voice Input
VoiceSec
  - Agent for voice/text recognition and security. Text input has safety mearures like locking after 3 minutes.
  - Possibility of using phone microphone that locally decodes the v2t and sends it to the VoiceSec API
  - Security measures

#### Headless Browser

#### Interpreter

## Fallbacks
You can setup fallbacks for disconnection or prompt refusal

## Anomaly Handling

## Terminal command recognition

# Control
For each project a package record will be kept from git to npm to anaconda to models and tensors to reduce and manage diskspace. Any downloaded file or package is hashed and tracked.
The ACC will try to use popular and stable packages and the most lightweight, the user is prompted when a certain threshold of package size is exceeded.

## Manage packages
The ACC will manage installed git repos and npm package versions with symlinks.


## Manage LoRa's

## Autonomous Config diff review


# Security
## Security Interpeter (SI)
Works between ACC and Interpreter and Contex handlers to determine if actions are allowed, if any security or potential safety issues might arise from the users instructions, and if any verbage can be interpreted in multiple ways or leave things to chance. The SI is responsible for negotiating between the Command(er) and the executive branch.

## Emergency & Safe word
Emergency actions like shutdown through shortcuts or safewords. For example while autonomously running things the user might want to interfere by pausing or shutting down the current tasks.

## Cascade detection, avoidance & termination
Detect whenever an initial vector starts deviating significantly in its core and try to avoid a cascading deviation stream that causes the initial vector to disappear. Terminate whenever a vector deviation does not match initial instructions.