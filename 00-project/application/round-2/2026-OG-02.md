---

name: Sodbayar Munkhsaikhan
neptun: KO4NHK
id: 2026-OG-02
--------------

# Implementation of a Consistent Dynamic Game World in a Text Adventure Based on Large Language Models

## My interpretation of the brief

The project is about creating a text-based adventure game in which the story and the game world change according to the player's decisions. The main challenge is to keep the world consistent during a longer gameplay session. Important information about characters, locations, objects, and events should be stored separately from the generated story. The LLM would use this information to generate appropriate narrative responses while the structured world state keeps track of what has actually happened.

## Why I am a good fit for this project

I am very interested in games, interactive applications, and artificial intelligence, especially in how AI can create more dynamic and personalized experiences. I find the idea of a game that can react differently to each player's decisions very interesting.

Although I do not currently have much practical experience with LLMs or AI application development, this is one of the main reasons why I am interested in this project. I would like to use the project as an opportunity to learn how LLMs work in real applications, how they can be connected to a program, and how information can be managed between the AI and the application.



## Relevant experience and background

I have basic programming knowledge from my university studies. However, I have not worked extensively with LLM APIs, AI-based applications, or long-term context and memory management.

I understand that there will be a learning curve for this project, but I am motivated to learn the required technologies step by step. I believe that starting with a small text-based game would make it possible for me to gradually understand the technologies and build the system in a manageable way.

## Proposed approach

I would start with a small and simple game world containing a limited number of characters, locations, objects, and important events. The game state would be stored in a structured form instead of relying only on the conversation history.

When the player makes a decision, the application would first update the relevant world state. The current state and the necessary context would then be provided to the LLM, which would generate the next part of the story.

This would allow the LLM to focus mainly on generating the narrative, while the application would be responsible for maintaining important facts and game state. I would also investigate different approaches for managing context and memory and compare them in terms of consistency, token usage, and scalability.

## Initial plan

First, I would learn the basic concepts required for using an LLM API and define the scope of a small text adventure. Then I would design the structured world model for characters, locations, objects, and events.

After that, I would implement basic player actions and connect them with the world state. I would then integrate an LLM and develop the communication between the application, the structured state, and the generated narrative.

The game would also support saving and continuing a session. Finally, I would test longer gameplay sessions and compare at least two approaches for context or memory management. The main goal of the evaluation would be to see how well the different approaches maintain consistency while controlling the amount of context sent to the LLM.

## Additional information
