This is a relatively simple Autogen project, consisting of a single file. Fair warning, I'm not a great developer :/ 

This uses heirarchical agent flow to pass to specific agents and separate out the groups into a cognition team and executive function team. 
https://github.com/microsoft/autogen/blob/main/notebook/agentchat_hierarchy_flow_using_select_speaker.ipynb

Some of the results of this model:
https://www.linkedin.com/posts/leah-bonser-72445522_ai-gpt4-chatgpt-activity-7134701494263586816-vOGV


Hypothesis: The “Hard work” of Artificial Intelligence is for the most part already complete with current gen LLMs.  Whilst they do not constitute a complete mind, the reasoning, decision making, 
empathy, psychological capabilities (eg: theory of mind), working memory and Understandings that are necessary prerequisites for an AGI are demonstrably in place already. 

The missing capabilities from LLMs notably include:
* Real time memory creation
* Translating working memory into episodic memory
* Long term memory formation
* Strong planning
* Credulity
* Belief creation
* Updating beliefs
* Explicit emotional functions
* Time sense and proprioception


Method:  We will provide neural “scaffolding” for the AGI using a combination of simple Python scripting, Microsoft Autogen, GPTs & Tooling, RAG and sundry cots software. 


System Design
The Core cognitive  process for Aretai is an Autogen group chat with key functions being performed by LLM Agents. The core Agents are:
Emotion - Detects and asigns emotions to messages inbound from the external world. Determines appropriate emotions to simulate in response to internal and external stimuli
Memory - Accesses beliefs, and episodic memory. This includes memory retrieval, updating and creation. This communicates with the NARs embeddings. 
Decision & Reasoning. The representative of rational, conscious thought. Makes decisions on how to act based on inputs from other systems. 
Planning. Executive functioning that provides an actionable steps to completing the decided action.
Ethics and Value Judgement. Assesses Decisions and plans to ensure that they align with Ethicals and Values. 
Goal Management. Complex multi-step plans need to be appropriately recorded. This agent communicates with the goal management sub system to create, update, remove etc goals as required.
Action. This sub system determines what external action to take based on the plan provided. This could be as simple as a text response, or theoretically, could involve complex code generation and control of a physical robotic platform. 

The benefit of Autogen is that the Agents and group Chat manager communicate flexibly in natural language. The externally callable functions (Memory, Action, goals etc) can be accessed as required as determined on the fly by the chat manager. 
Hopefully, this flexible cognitive model allows for a fair simulacra of intelligent behavior. 


Phase 1
** Framework
    * Custom groupchat separate cognition and executive functions
    * LLM independent  (Tested with Mistral & GPT 4)
** Agents:
    * Cognition
        * Self
        * Reasoning
        * Ethics
        * Creativity
        * Memory (including placeholder memories) 
        * Emotions
    * Exec Function
        * Exec manager
        * Judge / infosec
        * Speach (Text output)

Known Limitations: 
* The "memory" is just a short list of items in the system_message of the memory agent. there is only memory read, no write. Proper memory function is the core objective of phase 2. 
* The agent selection process is buggy and needs improvement. It does not always select the correct agent.
* Currently does not converse, just outputs a text speech string. 


