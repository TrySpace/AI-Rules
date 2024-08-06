# Coding and Language
The linguistic core of coding translated to human language. Most, if not all, coding concepts can be translated to words and descriptions; it is how we learn them. And it is how we instruct computers what to do.
LLMs have given us a tool to make the translation between this effortless and universal. Now we just need a standard structure of describing projects, essentially what business requirements are; so there is already a plethora of textual and visual tools to instruct what you want.
However, language, especially the human language we use on a daily basis relies on a lot of assumptive projections and vectors that are often implicit for humans, but not necessarily for computers, let alone LLMs; so it becomes imperative to know and curate what data an AI is trained in order to make the correct assumptions.
So the question becomes: does it need to know the whole body of work of Shakespeare to know how to correctly interpret your requests? Or rather the question should be: does a programmer need to have read Shakespeare for you to be able to communicate to them what they need to program? The answer is no. However could it be helpful for the AI to be able to create an app based on the description of "Romeo and Juliet"? Yes, but it can always read it on demand. Thus becomes the challenge to train specialized agents, or intelligent fragments to highly specific tasks without any noise from irrelevant contexts that it can always utilize later, or plug into.


# Code-to-Language
Creating a 1-to-1 mapping of existing code to minimal language files, that should be able to replicate the code by its' lingual description. This should provide any speaker of the language to modify the language and thus modify the code structure and behavior.
The main challenge would be to have a consistent generation of language from code and vice-versa.

# Language-to-Code
Especially initial project lingual descriptions would be exponentially complex and taper off when more detailed descriptions are added.
For example: "A todo app in javascript" and "A todo app in javascript with nosql" could trigger initially very different solutions, but as the description lenghens the overall vector of the project should narrow and large changes should decrease. Especially when more specificity is added the provided solutions should become increasingly 'clever' or more catered to the specific problem, and as more conditions and instructions are added the implementations should narrow down to the best possible solutions for the requests.