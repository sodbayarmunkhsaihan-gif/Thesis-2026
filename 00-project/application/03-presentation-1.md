---
project_outline: "[[00-project/01-project-outline]]"
---

<!-- 5xl -->
# Implementation of a Consistent Dynamic Game World in a Text Adventure Based on Large Language Models

Author: Sodbayar Munkhsaikhan  
Neptun: KO4NHK  
Supervisor: Gábor OLÁH  
Project ID: 2026-OG-02

---

<!-- 2xl -->
[prmd.atom-forge.eu/docs](https://prmd.atom-forge.eu/docs)

---

## Problem

Large language models (LLMs) can generate interesting stories and dialogues, but they may forget or change important information during longer gameplay.

For example, a character may appear in a different location without explanation, or an object may be forgotten after the player has picked it up.

This project aims to reduce these inconsistencies by storing important game-world information separately and using it when generating the next part of the story.

---

## Target users

- Players who enjoy interactive, text-based adventure games.
- Players who want their decisions to influence the story and game world.

The project supervisor and university are also stakeholders because they guide and evaluate the project.

---

## Planned scope

### In scope

- Generate stories and dialogues using an LLM.
- Let players make decisions that affect the story.
- Manage characters, locations, objects, and important events separately.
- Keep the generated story consistent with the stored game state.
- Save and load game sessions.
- Handle basic logical contradictions.

### Out of scope

- Multiplayer gameplay.
- Complex 3D graphics.
- AI-generated images.
- Advanced independent memory for multiple characters.

The first version will focus on a small, text-based adventure with the essential features working reliably.

---

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
3. The system stores the current game state.
4. The player loads the saved game later.
5. The adventure continues from the saved state.

---

## Next steps

- Finalize the functional requirements and acceptance criteria.
- Design the structured game-world model.
- Research and compare at least two LLM context or memory-management approaches.
- Decide how the application will communicate with the LLM.
- Prepare the initial technical design and implementation plan for semester 2.
