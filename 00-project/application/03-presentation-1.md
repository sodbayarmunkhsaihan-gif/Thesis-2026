⸻

project_outline: “[[00-project/01-project-outline]]”

<!-- @slide Title -->
<!-- 5xl -->

Implementation of a Consistent Dynamic Game World in a Text Adventure Based on Large Language Models

Author: Sodbayar Munkhsaikhan
Neptun: KO4NHK
Supervisor: Gábor OLÁH
Project ID: 2026-OG-02

⸻

<!-- @slide Problem -->
<!-- @layout AAB -->

Problem

<!-- @set-align left -->

* LLMs can generate interesting stories and dialogues.
* During long adventures, they may forget or change important facts.
* For example, a key may still appear on a table after the player picks it up.
* This makes the game world inconsistent and player choices less meaningful.

<!-- @callout question -->

How can an LLM generate a flexible story while keeping important game facts consistent?

⸻

<!-- @slide Project idea -->

From player decisions to a consistent story

flowchart TD
    P["Player action"] --> V["Check action"]
    V --> S["Update world state"]
    S --> C["Provide relevant facts"]
    C --> L["Generate next story"]
    L --> P

The application stores important game facts separately from the story.

For example, when the player picks up a key, the application updates its location to the player’s inventory. The LLM receives this information before generating the next story.

<!-- @note -->

World state: Information about the current game, including characters, locations, objects, inventory, and important events.

⸻

<!-- @slide Target users -->

Target users

<!-- @set-align left -->

Players who enjoy interactive text adventures.

They want to:

* Make meaningful choices.
* Explore a consistent game world.
* Save and continue later.
* See the story change with their decisions.

Other stakeholders: The supervisor and university evaluate the project.

⸻

<!-- @slide Planned scope -->

Planned scope

<!-- @set-align left -->
<!-- @columns 2 4 -->

In scope

* LLM-generated stories
* Player choices and world changes
* Characters, objects, and locations
* Basic consistency checks
* Save and load
* Compare two memory approaches
* Test key functions

<!-- @col-break -->

Out of scope

* Multiplayer
* 3D graphics
* AI-generated images
* Automatically created large worlds
* Complex NPC memory

<!-- @columns -->

The first version will be a small, single-player adventure.

⸻

<!-- @slide Rules -->

Rules behind the game world

<!-- @set-align left -->

* The application controls important facts.
* Actions are checked before the world changes.
* Important facts stay consistent. An object cannot be in two places at once.
* The story uses the current world state. The LLM receives relevant information before generating the next part.
* Saving preserves progress. Loading restores the game state, not just the story text.

<!-- @note -->

These are planned design rules. The project will investigate how to detect and handle contradictions between the generated story and the stored world state.

⸻

<!-- @slide Initial user journeys -->

Initial user journeys

flowchart TD
    A["Start game"] --> B{"New or saved?"}
    B -->|New| C["Generate opening story"]
    B -->|Saved| D["Restore game state"]
    C --> E["Choose action"]
    D --> E
    E --> F["Update world state"]
    F --> G["Generate next story"]
    G --> H{"Continue or save?"}
    H -->|Continue| E
    H -->|Save| I["Save game state"]

1. Start and play

1. Start a new game.
2. Read the opening story.
3. Choose an action.
4. Update the world state.
5. Generate the next story.

2. Save and continue

1. Save the current game.
2. Store the world state.
3. Load the game later.
4. Continue from the saved state.

⸻

<!-- @slide Research and next steps -->

Research and next steps

<!-- @set-align left -->

1. Define the world model: characters, objects, locations, and events.
2. Compare two memory approaches: consistency, token usage, and scalability.
3. Plan LLM context: choose relevant facts and conversation history.
4. Plan consistency and saving: handle invalid actions and restore saved games.
5. Prepare for Semester 2: choose technologies and plan implementation.

This semester focuses on the specification and technical plan.

⸻

<!-- @slide End -->

Thank you

Questions and feedback are welcome.
