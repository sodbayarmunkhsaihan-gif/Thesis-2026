---
project_outline: "[[00-project/01-project-outline]]"
---

<!-- @slide Title -->

<!-- 5xl -->

# Implementation of a Consistent Dynamic Game World in a Text Adventure Based on Large Language Models

Author: Sodbayar Munkhsaikhan  
Neptun: KO4NHK  
Supervisor: Gábor OLÁH  
Project ID: 2026-OG-02

---
<!-- @slide Problem -->
<!-- @layout AAB -->

## Problem

<!-- @set-align left -->

- Large language models (LLMs) can generate **interesting stories and dialogues**.
- During a long adventure, an LLM may **forget or change important facts**.
- For example, the player picks up a key, but later the story describes the key as still lying on the table.
- This can make the game world feel **inconsistent** and make player decisions less meaningful.

<!-- @callout question -->

> How can we let an LLM generate a flexible story while keeping the important facts of the game world consistent?

---
<!-- @slide Project idea -->

## From player decisions to a consistent story


The application stores important facts separately from the generated story.

For example, when the player picks up a key, the application updates its location to the player's inventory. The LLM then receives this information when generating the next part of the story.

<!-- @note -->

> **World state:** structured information about the current game, such as character locations, objects, inventory, and important events. The LLM generates the story, while the application keeps track of the actual game state.

---
<!-- @slide Target users -->

## Target users

<!-- @set-align left -->

<!-- @set-width 70% -->

**Players** who enjoy interactive, text-based adventure games and want their decisions to influence the story and game world.

Players want to:

- Make choices that have meaningful consequences.
- Explore a world with consistent characters and objects.
- Save their progress and continue later.
- Experience a story that responds to previous decisions.

The project supervisor and university are also stakeholders who evaluate the project's design and implementation.

---
<!-- @slide Planned scope -->

## Planned scope

<!-- @set-align left -->

<!-- @columns 2 4 -->

### In scope

- LLM-generated stories and dialogue
- Player decisions that change the world
- Structured characters, locations, objects, and events
- Basic consistency and contradiction handling
- Saving and loading game sessions
- Comparison of two context or memory approaches


<!-- @col-break -->

### Out of scope

- Multiplayer gameplay
- Complex 3D graphics
- AI-generated images
- Large worlds created automatically by the game
- Complex memory systems for many non-player characters (NPCs)

<!-- @columns -->

The first version will focus on a small, single-player adventure with the essential features working reliably.

---
<!-- @slide Rules -->

## Rules behind the game world

<!-- @set-align left -->

- **The application controls important facts.** The LLM does not independently decide the stored world state.
- **Actions are checked before the game state changes.** Invalid actions should not lead to impossible situations.
- **Important facts must stay consistent.** For example, an object cannot be in the player's inventory and on a table at the same time.
- **The story uses the current world state.** The LLM receives relevant information before generating the next part.
- **Saving keeps the player's progress.** When a game is loaded, the important game information should be restored, not just the story text.

<!-- @note -->

> These are planned design rules, not implemented or tested features yet. One research question is how to find and handle contradictions when the LLM generates a story that does not match the current game state.

---
<!-- @slide Initial user journeys -->

## Initial user journeys

### Journey 1: Start and play

1. The player starts a new adventure.
2. The system generates the opening story.
3. The player chooses an action.
4. The system updates the game-world state.
5. The LLM generates the next part of the story using relevant information.

### Journey 2: Save and continue

1. The player makes decisions and changes the game world.
2. The player saves the game.
3. The system stores the current game state and player loads it and continues.

 
---
<!-- @slide Research and next steps -->

## Research and next steps

<!-- @set-align left -->

<!-- @set-width 80% -->

1. **Define the world model:** decide how characters, locations, objects, inventory, and events will be represented.
2. **Compare two context or memory approaches:** evaluate consistency, token usage, and scalability.
3. **Define the LLM interaction:** decide which world information and conversation history should be sent to the LLM.
4. **Plan consistency checks and saving:** decide how to prevent invalid changes to the game state and how to save and load games.
5. **Prepare for Semester 2:** select suitable technologies and implement the planned core features.


---
<!-- @slide End -->

## Thank you

Questions and feedback are welcome.
