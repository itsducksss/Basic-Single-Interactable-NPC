# Basic Single Interactable NPC Dialouge Tutorial
Description

This is a Unity tutorial for an interactable NPC, and how to create a basic single lined dialouge system.

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed. This is as the changes in the updates can cause errors to occur that may have been fixed or changed within different versions of the Unity and Visual Studio softwares.

If you need help installing Unity you can find many online tutorials such as: https://learn.unity.com/tutorial/install-the-unity-hub-and-editor

You will also need to know how to create an empty project, add primitive objects to your scene, create blank scripts, and run projects from within the editor. If you need help with this, there is a short video demonstrating how to do all of these things here:

https://www.youtube.com/watch?v=eQpWPfP1T6g

# Primary Objectives
This tutorial aims to create a simple interactable NPC, which means that if an specific input (which is the "F" key for this tutorial) occurs within a set distance from the NPC, another specified action will occur. The action for this tutorial is a simple "Hi" popup which will be created using Unity's UI system.

# Preview

https://github.com/user-attachments/assets/48434107-7236-4910-86e4-8412b547e3a9

# Getting Started
To start this tutorial, we will need to create a new Unity Project. To the Unity scene we will add a Plane to represent the floor, and 2 capsules to represent the NPC and the Player, see image below.

![image](https://github.com/user-attachments/assets/acf9d0b9-9cad-479d-b816-67c8ad6909bb)![image](https://github.com/user-attachments/assets/a2553329-ee27-4e43-be49-3f40597590fe)

For this tutorial in the images shown throughout, the Player is shown as the green capsule, while the NPC is shown as the Red capsule. The functions relating to the NPC and Player will also be depicted with these colours. It is best to rename the capsules, Player and NPC so that it is easier to organise within the Unity heirarchy. Before any coding or changes to the Unity scene it is best to run the scene to ensure there are no underlying problems with the scene itself prior to the tutorial that may affected. For this tutorial it is best to have a movable character to see if some components fo this tutorial work within the area wanted.

For this tutorial we can break it into 4 smaller objectives/ tasks and then combine them to complete the tutorial and achieve the desired results.
1. To create and code a sphere that will detect the player.
2. To create the UI for the dialouge.
3. To combining the previous tasks to create an NPC with a player detect sphere that allows the player to inteact with them, and show a dialouge popup on screen.

This tutorial will follow the layout stated above.

# Making sphere that detects the player

![image](https://github.com/user-attachments/assets/06f481b0-12c2-4442-9b3a-fdaeb90db614)

Looking at the Unity scene, we will first create a sphere with the same transforms of the NPC capsule this will mean that the NPC is within the centre of the sphere. The transform component is used to show where an object is (in this case the capsule) within the scene, and maintaining and or chaning its position. To maintain the position of the capsule, we do not have to add an input. To change the position of the capsule we can alter the values within the position boxes of the transform components. This will change where the capsule is within a specific axis. To make the sphere and the NPC to have the same position, we can copy and paste the transforms of the NPC onto the newly created sphere.
![image](https://github.com/user-attachments/assets/1eb0fbdf-b5c3-4daa-b80c-e7aa491fc2f3)![image](https://github.com/user-attachments/assets/e93cd4ba-4c63-483f-b6b7-3814ea6b998e)


To make the sphere and the NPC to have the same position, we can copy and paste the transforms of the NPC onto the newly created sphere. We then scale up the size of the sphere to the desired sized of the interactable area of the NPC to have. We will then rename the sphere as Player Detect, as this is will detect the player.

![image](https://github.com/user-attachments/assets/19863ec6-153a-4425-a8ad-a78f9f6859a1)

https://github.com/user-attachments/assets/9c5c8842-2bf5-4687-8bdd-ea19fe481e35

I will create a new material (semi-transparent), by adjusting the emission (tick the emission box within the Inspector Window of the new material) of the material so that the NPC can still be seen with it covering the NPC capsule. I will then apply a material onto the sphere to make it easier to visually understand where the boundaries for the player can interact with the NPC. 

![image](https://github.com/user-attachments/assets/8e39e6a6-9fee-4f38-bcd2-edcb1767c2aa)![image](https://github.com/user-attachments/assets/2f735892-7083-471d-8250-38f7df3dbadc)

This can be done, by dragging and dropping the material into the sphere's Inspector Window. We will the drag the Player Detect (sphere) into the NPC so that they are connected. The NPC capsule will be the parent, with the sphere will be the child of the NPC.
![image](https://github.com/user-attachments/assets/fc3ba100-f3ab-4649-9d6e-cb31967e3968)
We will then create a script called NPCSystem onto the Player Detect. For this tutorial only the Player Detect will have a script and not the NPC itself.

![image](https://github.com/user-attachments/assets/c7d9d4b2-736c-4751-8d27-7268768a1566)
-  using [insert system] means that it can refer to that specific system and its properties when coding using references made to a specific system
- : means this class inherits functions and variables from another class
- Monobehaviour refers Unity supplied class that attaches directly to GameObjects, which we base a new class onto.
- bool refers to a value that is either true or false.
- player_detection refers to the
- && means
- false means
- ; is used at the end of most lines/ statements FIXX DIS
- void refers to a function can return normally without the need of a value.
- update means a function that gets called every frame if the MonoBehaviour is enabled.
- Input means
- GetKeyDown means that an action will occur when a key is pressed down
- KeyCode.F this refers to a specific key in this case the F key. If it was KeyCode.E it would refer to the E Key.
- print("-") is an action in which the whatever is within the ("-") will be shown in the console.
- private
- if() is an if statement which is
- Collider other
- other.name
- == this means that the equation/ value that is used to perform this action is true/ equal
- "Player" is the tag that we used to help identify which game object is the player.
- OnTriggerExit
- {} is what is used to

![image](https://github.com/user-attachments/assets/e92ae03f-d562-43da-aae5-bebaa06c0a58)
Before we play the scene, we make sure that the Player detect sphere has a sphere collider. We then edit the collider so that the collider is a trigger that means that it has the abilities to trigger another action to occur.


https://github.com/user-attachments/assets/de4cbb52-bfe5-4d67-bb42-61330bdd5298


When playing the scene this should be the result. The console should have whatever message you typed in the print("-") in this case - would shouw in the console.
