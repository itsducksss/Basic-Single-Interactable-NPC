# Basic Single Interactable NPC Dialouge Tutorial FIXXXXXXXXXXX SCRIPT NO WORKKKK FOR MOVE
Description

This is a Unity tutorial for an interactable NPC, and how to create a basic single lined dialouge system.

# Prerequisites
Before approaching this tutorial, you will need a current version of Unity and a code editor (such as Microsoft Visual Studio Community) installed and ready to use.

This tutorial was created with Unity 2022.3 LTS and Microsoft Visual Studio Community 2022 versions. It should work with earlier or later versions. But you should check the release notes for other versions as the Editor controls or Scripting API functions may have changed. This is as the changes in the updates can cause errors to occur that may have been fixed or changed within different versions of the Unity and Visual Studio softwares.

If you need help installing Unity you can find many online tutorials such as: https://learn.unity.com/tutorial/install-the-unity-hub-and-editor

You will also need to know how to create an empty project, add primitive objects to your scene, create blank scripts, and run projects from within the editor. If you need help with this, there is a short video demonstrating how to do all of these things here:

https://www.youtube.com/watch?v=eQpWPfP1T6g

# Primary Objectives
This tutorial aims to create a simple interactable NPC, which means that if an specific input (which is the "F" key for this tutorial) occurs within a set distance from the NPC, another specified action will occur. The action for this tutorial is a simple "Hi" popup which will be createsd using Unity's UI system.

# ADD PREVIEW

# Getting Started
To start this tutorial, we will need to create a new Unity Project. To the Unity scene we will add a Plane to represent the floor, and 2 capsules to represent the NPC and the Player, see image below.

![image](https://github.com/user-attachments/assets/acf9d0b9-9cad-479d-b816-67c8ad6909bb)![image](https://github.com/user-attachments/assets/a2553329-ee27-4e43-be49-3f40597590fe)

For this tutorial in the images shown throughout, the Player is shown as the green capsule, while the NPC is shown as the Red capsule. the functions relating to the NPC and Player will also be depicted with these colours. Before any coding or changes to the Unity scene it is best to run the scene to ensure there are no underlying problems with the scene itself prior to the tutorial that may affected.

or this tutorial we can break it into 4 smaller objectives/ tasks and then combine them to complete the tutorial and achieve the desired results.
1. To create a movable player.
2. To create and code a sphere that will detect the player.
3. To create the UI for the dialouge.
4. To combining the previous tasks to create an NPC with a player detect sphere that allows the player to inteact with them, and show a dialouge popup on screen.

This tutorial will follow the layout stated above.

# Moving the character
Looking at the Unity scene, and selecting the capsule on the right hand side of the screen in the Inspector Window, we can see a the properties of the capsule. At the top of the Inspector window shows the attributes of the Transform  component of the capsule.
![image](https://github.com/user-attachments/assets/1fc638d7-4de4-48d6-81ca-aa8fb04e86c1)

The transform component is used to show where an object is (in this case the capsule) within the scene, and maintaining and or chaning its position. To maintain the position of the capsule, we do not have to add an input. to change the position of the capsule we can alter the values within the position boxes of the transform components. this will change where the capsule is within a specific axis.
![image](https://github.com/user-attachments/assets/a2553329-ee27-4e43-be49-3f40597590fe)![image](https://github.com/user-attachments/assets/baf98287-29ab-44eb-82f3-c1ad04f638d3)

This image shows how the position is changed in the x axis by changing the value of the x in the Inspector Window.
This means that to move the player, all we have to do is create a script that allows for the gameObjects' transform to change depending on the input.

# Scripting Player Movement
First we must select the Player capsule, in the Inspector Window select create and add new script and name it PlayerMovement. When writing scripts, the Name of a script must be written out in one word, with capital letters to indicate a space. This means PlayerMovement will show in the Inspector Window as Player Movement.

![image](https://github.com/user-attachments/assets/a9020ef4-3ad8-4256-91bb-b7bc320f9400)

We will then double click the script added, and that should load up Microsoft Visual Studio (or any other coding software on your device). This is what will appear.

![image](https://github.com/user-attachments/assets/08ebb3bd-df01-48b7-a1de-953244919ae5)
- using [insert system] means that it  can refer to that specific system and its properties when coding using references made to a specific system.
- public means that this class can be accessed from other scripts.
- class means that what follows is a class definition.
- : means this class inherits functions and variables from another class
- Monobehaviour refers Unity supplied class that attaches directly to GameObjects, which we base a new class onto.
- void refers to a function can return normally without the need of a value.
- start means that it is enabled just before any of the Update methods are called the first time, when the Monobehaviour is enabled.
- update means a function that gets called every frame if the MonoBehaviour is enabled.

![image](https://github.com/user-attachments/assets/7f8c8028-9eee-46fd-9ad0-17ef91b3166c)
- Rigidbody refers to a component you can add to a gameObject that allows for a physics-based way to control the movement and position of a GameObject.
- rb is what it will be called within the script. this means that when we type in rb that the Rigidbody will be referenced.
- [SerializedField] helps to make the private variables accessible within the Unity editor without making them public, as well as helps to make serialize any private variable.
- GetComponent means that when this action or statement is refered to that unity will detect this component from the object that the script is applied onto and use it to complete that certain action. In this case it means that when rb is mentioned that at the start of the scene that unity will get that component, and use it in the void update statement to move using the Rigidbody component on the capsule/ player.
- float refers to a numerical value that can be assigned (whole or decimal).
- MoveSpeed what the float (previous point) will be refered to within the code. This means that when y = x * MoveSpeed, that y is equal to the value of x multiplied by the MoveSpeed/ float which is 10 in the script.
- horInput refers to the total value calculated of the Input by the user on the horizontal axis multiplied by the MoveSpeed.
- verInput refers to the total value calculated of the Input by the user on the vertical axis multiplied by the MoveSpeed.
- GetAxiRaw("-") refers to the axis (Horizonal or Vertical) which uses the world's x and z axis using the Left and Right, and a and d keys.
- rb.velocity, it refers the velocity vector of the rigidbody.  it represents the rate of change of the rigid body per frame.
- new just means new
- Vector3 refres to the position using all 3 axis x, y, z which can be represented on a 3d space.

To customise the results of the script you can adjust the number of the float in the script higher to increase the movement speed and lower to decrease the movement speed.

# ADD IN RESULTS OF SCRIPT and more detail pls.




