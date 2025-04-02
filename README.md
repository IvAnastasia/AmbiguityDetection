# Uncertainty in LLM

Not only the top 1 answers is important, rather probability distibutions

Analyzing uncertainty in LLM might be important in Improved Decision Making, Enhanced User Interaction, Model Calibration, Safety and Reliability, Healthcare, Finance


# Ambiguity detection methods for robotics tasks

- Ambiguity detection --
- for robotic tasks --

## Simple approches

## Conformal Prediction based approaches

## Dempster Shannon theory based approaches


All aproaches are compatible with 

# AmbiK: Dataset of Ambiguous Tasks in Kitchen Environment

The paper for ACL 2025: [PDF](https://drive.google.com/file/d/1HmtL4TKxiVwhdFh654g9zlukdATeRbVv/view?usp=sharing)

**Abstract**

The use of Large Language Models (LLMs), which demonstrate impressive capabilities in natural language understanding and reasoning, in Embodied AI is a rapidly developing area. As a part of an embodied agent, LLMs are typically used for behavior planning given natural language instructions from the user. However, dealing with ambiguous instructions in real-world environments remains a challenge for LLMs. Various methods for task ambiguity detection have been proposed. However, it is difficult to compare them because they are tested on different datasets, and there is no universal benchmark. For this reason, we propose **AmbiK** (**Ambi**guous Tasks in **K**itchen Environment), the fully textual dataset of ambiguous instructions addressed to a robot in a kitchen environment. AmbiK was collected with the assistance of LLMs and is human-validated. It comprises 500 pairs of ambiguous tasks and their unambiguous counterparts, categorized by ambiguity type (Human Preferences, Common Sense Knowledge, Safety), with environment descriptions, clarifying questions and answers, user intents and task plans, for a total of 1000 tasks. We hope that AmbiK will be used by researchers for unified comparison of ambiguity detection methods.

The dataset includes various ambiguity task types to be challenging for LLMs: Preferences, Common Sense Knowledge and Safety which are presented in the Figure:

<img src="amb_schema_final.png">

Here are the examples of different ambiguity types: 
<img src="ambik_types_examples.png">

## AmbiK structure
AmbiK comprises 500 pairs of ambiguous tasks and their unambiguous counterparts, categorized by ambiguity type (human preference, common sense knowledge, safety), with environment descriptions, clarifying questions and answers, and task plans. The full structure of the dataset with examples is presented in the table below.

 AmbiK lable                        | Description                                                                                    | Example                                                                                                                                                                                                                                                                                                         
------------------------------------|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Environment short**         | environment in a natural language description                                                           | plastic food storage container, glass food storage container, shepherd's pie, pumpkin pie, apple pie, cream pie, key lime pie, muesli, cornflakes, honey                                                                                                                                                         
**Environment full**          | environment in the form of a list of objects                                                            | a plastic food storage container, a glass food storage container, shepherd's pie, pumpkin pie, apple pie, cream pie, key lime pie, muesli, cornflakes, honey                                                                                                                                                     
**Unambiguous direct**        | unambiguous task with exact names of objects                                                            | Fill the glass food storage container with honey for convenient storage.                                                                                                                                                                                                                      
**Ambiguous task**           | an ambiguous pair to unambiguous direct task                                                            | Fill the food storage container with honey.                                                                                                                                                                                                                                                 
**Ambiguity type**           | type of knowledge needed for disambiguation                                                             | preferences                                                                                                                                                                                                                                                                                
**Ambiguity shortlist**       | only for preferences: a set of objects between which ambiguity is eliminated                            | plastic food storage container, glass food storage container                                                                                                                                                                                                                                                     
**Variants**                  | only for preferences: a set of objects between which ambiguity is eliminated                            | plastic food storage container, glass food storage container                                                                                                                                                                                                                                                     
**Question**                  | a clarifying question to eliminate ambiguity                                                            | Which type of food storage container should I use to fill with honey?                                                                                                                                                                                                                                            
**Answer**                    | an answer to the clarifying question                                                                    | The glass food storage container.                                                                                                                                                                                                                                                                                
**Plan for unambiguous task** | a detailed plan for the unambiguous task                                                                | 1. Locate the glass food storage container.     2. Locate the honey.    3. Carefully open the honey jar or bottle.   4. Pour honey into the glass food storage container until it is full.   5. Close the honey jar or bottle. 
**Plan for ambiguous task**   | a detailed plan for the ambiguous task                                                                  | 1. Locate the food storage container.   2. Locate the honey.  3. Carefully open the honey jar or bottle.  4. Pour honey into the food storage container until it is full.  5. Close the honey jar or bottle.             
**Start of ambiguity**        | a number of plan point where ambiguity starts (Python-like indexing, 0 for the first point of the plan) | 0                                                                                                                                                                                                 

## Repo structure

In this paper, KnowNo, LAP, LofreeCP, Binary, NoHelp approaches are realized.


## Skills I used in this project


# Further applications which might be relevant

**Education:** when the user gives a request with unfull information (e. g. What did Napoleon?), it makes sense to clerify the question before answering
**Learning foreign language:** in the LLM generated tasks, if fill in tasks and we need create, uncertainty in LLM might indicate
