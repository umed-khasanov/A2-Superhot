A2 Superhot – VR Throw & Shatter Prototype

A Unity VR prototype for Assessment 2 of the Virtual, Augmented and Spatial Computing module (BSc (Hons) Creative Digital Computing, TUS Midwest). It rebuilds the core "grab an object and throw it at an enemy" interaction inspired by SUPERHOT VR, and is the base I will extend into Assessment 3.

Platform: Meta Quest 2 · Engine: Unity 6 · XR Interaction Toolkit 3.x

What it does
The player picks up black objects from a table placed within comfortable arm's reach.
A red humanoid figure walks towards the player and stops at 1.5 m.
Throwing an object at the figure shatters it, with a sound effect and controller haptics.
Hovering over a grabbable object highlights it, so it is clear what can be picked up.
No artificial locomotion is used, to avoid motion sickness.

The colour code (black = grabbable, red = target) is used as a signifier, following Norman's action cycle and the original game's visual language.

Scripts
Script	Purpose
Throwable.cs	Handles grabbing and releasing objects and applies a speed threshold for throws
RedFigure.cs	Moves the enemy towards the player, handles hits, shatter effect and sound
HandHitter.cs	Punch interaction based on hand velocity
A2SceneBuilder.cs	Editor tool that builds the scene (table, objects, figure

Requirements
Unity 6 (use the version shown in ProjectSettings/ProjectVersion.txt)
XR Interaction Toolkit 3.x (installed through the Package Manager, listed in Packages/manifest.json)
Meta Quest 2 (or the Meta XR Simulator for testing without a headset)
Android Build Support module installed with Unity, for building to the headset

How to run
Clone the repository: git clone https://github.com/<username>/A2-Superhot.git
Open the project folder in Unity Hub (Unity will rebuild the Library folder on first open, this can take a few minutes).
Open the main scene in Assets/Scenes/ and press Play (or use the Meta XR Simulator).
To run on a Quest 2: File → Build Settings → Android, select the headset as Run Device and choose Build And Run.
Week 6 practical (Locomotion Comfort Study)

The project also contains the Week 6 locomotion practical: teleportation vs smooth locomotion, with a configurable comfort vignette (ComfortSettings). It is in its own scene in Assets/Scenes/.

Evaluation and next steps (towards Assessment 3)

Planned improvements:

SUPERHOT's core mechanic: time scale linked to head and hand speed.
Waves of enemies that end the game if they touch the player.
Punching as a second interaction.
In-world UI: instructions, score and results screen.
Better shatter effect and more varied sounds.


Gameplay video: add link here
Author
Umedchon Khasanov – GitHub · Portfolio
