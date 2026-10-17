---

name: Sodbayar Munkhsaikhan
neptun: KO4NHK
id: 2026-OG-02
github:https://github.com/sodbayarmunkhsaihan-gif/Thesis-2026.git
github_project:https://github.com/users/sodbayarmunkhsaihan-gif/projects/2
---------------

# Implementation of a Consistent Dynamic Game World in a Text Adventure Based on Large Language Models

This project implements a text-based AI adventure game in which the story changes according to the player's decisions. A large language model is used to generate the story, dialogue, and descriptions, while the application separately manages important game-world information such as characters, locations, objects, and events. The project aims to keep the game world consistent during longer gameplay sessions and allow the player to save and continue their progress.

## Objectives

* **Primary objective:** Develop a functional text-based adventure game that combines LLM-generated storytelling with structured game-world state management.
* **Target users / stakeholders:** Players who enjoy interactive text-based adventure games; the project supervisor and university/course are also stakeholders.
* **Measurable success criteria:** A player can start a game, make decisions that affect the story and game world, save the game, and load it later while important world-state information remains consistent.
* **Constraints:** Use an LLM API or local model; persist important game-world state; test important state-management functions; use Git for version control; no credentials or secret keys in the repository.

## Scope

### In scope

* Starting and playing a text-based adventure.
* LLM-generated story, dialogue, and descriptions.
* Player decisions affecting the story and game world.
* Structured management of characters, locations, objects, and important events.
* Saving and loading game sessions.
* Basic handling of logical contradictions.
* A usable game interface.
* Comparison of at least two context or memory-management approaches.

### Out of scope

* Multiplayer gameplay.
* Complex 3D graphics.
* AI-generated images.
* Online social features.
* Large procedurally generated worlds.
* Advanced independent memory systems for multiple NPCs.

## Notes

The first version will focus on a small and manageable text-based adventure with a limited game world. The main focus will be keeping important world information consistent while the LLM generates the story. Additional features may be considered only after the core gameplay and state-management functionality are working reliably.
