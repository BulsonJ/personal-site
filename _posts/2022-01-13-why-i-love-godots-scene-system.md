---
layout: post
title:  "Why I Love Godot's Scenes"
category: blog
---
For just under a year now, I have been using Godot. Over that time, I've gained a lot of familarity with it. While working with it, I've grown to love using Godot's scene system to create my games. It allows for a lot of flexibility and modularity. Previously, I had tried using lots of hardcoded logic and inheritance to allow for code reusability, but I found it tricky to work with.

For those new to Godot, Godot uses a node and scene system. Each scene is built up of a tree of nodes. Nodes are the building blocks within Godot. They have a name, can have a script, and can also have child nodes attached. There are many different type of nodes which provide different functionality, such as the Label node which allows you to write text to the screen, or the KinematicBody2D node which provides useful functions for moving a physics body. A scene consists of a root node and a group of nodes that are organised in a tree hierarchy. 

In Godot, when you run your game, you run a scene. For example, this scene would consist of nodes for the player, the obstacles, the UI and so on. However, what makes the scene system powerful is that scenes can also instance other scenes inside of them. So, in the example scene above, the player could be a single instanced scene. Then, inside of the player scene could be a Sprite node(Used to display the player), an AudioStreamPlayer node(Used to play audio) and more. 

Currently for the prototype I have been creating, I've been taking advantage of the scene system, and creating scenes which are much more flexible and allow for more reusability. For the majority of these scenes within my prototype, I have called them 'components' as they are the building blocks behind a lot of my entities. These components can be attached to provide functions or behaviour to an object. This is similar to Unity's GameObject and script system, and how you can attach multiple scripts to a GameObject. 

Below is an example of an enemy prototype I have created in my game:

![EnemyScene](/assets/images/2022_01_13-GodotScene.png)

Each of these components can hold state, used to call functions and/or communicate with other components. Their logic is self-contained and can be easily attached to and removed from entities.  I used export variables in the components to make use of Dependency Injection. These variables specify the path of the component nodes and is used where components need to access other component's state or connect to their signals. 

I also used it to provide a way for default behaviour to be enabled by components. For example, a HealthComponent and a HitboxComponent are attached to the enemy. If the HealthComponent has the path of the HitboxComponent, it will automatically remove health when the HitboxComponent registers a damage hit. I could code this behaviour in the Enemy script, but this would have to be done in every script for an entity that has both these components. 

This would not be possible without the scene system provided by Godot. It allows me to abstract away complexity inside of a single node and provides a great system so that I can create a large portion of entities's functionality through composition.


