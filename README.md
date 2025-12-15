# RiseUp 

> A polished "Vertical Slice" of a 2D vertical platformer developed in **Unreal Engine 5**.

![Unreal Engine](https://img.shields.io/badge/Engine-Unreal_Engine_5.6-black?style=flat&logo=unrealengine)
![Language](https://img.shields.io/badge/Language-Blueprints-blue?style=flat)

## About The Project

**RiseUp** is a 2D platformer where the goal is simple: **Climb**. Inspired by classics like *Super Mario Bros.* and modern hits like *Celeste*, the game focuses on "Game Feel"—prioritizing responsive, momentum-based movement and fair combat.

This project was developed as a capstone engineering challenge to demonstrate the viability of creating high-fidelity 2D games using **Unreal Engine 5** and the **Blueprint Visual Scripting** system.

### Key Features
* **Vertical Locomotion System:** Physics tuned for "snappy" controls, including "Coyote Time" (jump buffering) and momentum conservation.
* **Active Combat:** Unlike many "tower climbers" that feel empty, RiseUp features active enemy AI that must be defeated or bypassed.
* **Modular Level Architecture:** A scalable system that loads level "chunks" asynchronously, allowing for infinite vertical expansion.
* **Persistent Progression:** Utilizes a Singleton architecture to track run timers and music states seamlessly across level transitions.

---

## 🎮 Controls

The game is designed for Keyboard & Mouse input.

| Action | Input |
| :--- | :--- |
| **Move Left / Right** | `A` / `D` |
| **Jump** | `Spacebar` (Hold for higher jump) |
| **Attack** | `Left Click`, `Q`, or `Shift` |
| **Pause / Quit** | `Esc` |

---

##  Tech Stack & Architecture

This project pivoted from an initial Godot C# proposal to **Unreal Engine 5** to leverage industry-standard tools.

* **Engine:** Unreal Engine 5.3
* **Scripting:** Blueprint Visual Scripting
* **Animation:** [PaperZD](https://github.com/Graeme_Robinson/PaperZD) (State Machine Plugin) 
* **IDE:** Visual Studio 2022 (for C++ interfacing) 

### Design Patterns Used
* **Singleton Pattern:** Implemented via `GameInstance` to manage global game state and audio persistence
* **State Pattern:** Managed via PaperZD to handle complex character animations (Idle -> Run -> Jump -> Fall -> Defeated) without spaghetti code.
* **Inheritance:** `BP_Adventurer` (Player) and `BP_Pig` (Enemy) share a common `BP_Character` parent for physics and health logic.

---

## Installation & Setup

No installation of Unreal Engine is required to play the release build.

1.  **Download:** Download `Windows-RiseUp.zip`.
2.  **Extract:** Unzip the contents to a folder on your computer.
3.  **Play:** Navigate to the folder and launch `sideScroller.exe`.

> *Note: If Windows Defender prompts a warning, select "More Info" -> "Run Anyway" (The executable is not digitally signed).*

---

## 🐛 Debugging & Testing
The project underwent rigorous "Black Box" testing and unit debugging using the Unreal Blueprint Debugger.
* **Fixed Issues:**
    * *Floaty Physics:* Gravity Scale increased to 3.5 for snappier fall speeds.
    * *AI Pathfinding:* Implemented Raycast `CheckLedge()` functions to prevent enemies from walking off platforms.

---

## 📜 Credits & Attribution

* **Developer:** Felipe Galeano
* **Plugins:** [PaperZD](https://www.criticalfailure-studio.com/paperzd-documentation/) by Critical Failure Studio.
* **Assets:** Various free marketplace assets used for environmental visuals.



