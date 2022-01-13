---
layout: post
title:  "Why I Love Godot's Scenes"
category: blog
---
<p>For just under a year now, I have been using Godot. Over that time, I've gained a lot of familarity with it. While working with it, I've grown to love using Godot's scene system to create my games. It allows for a lot of flexibility and modularity.</p>

<p>For the game I'm currently developing(link here), I feel like I've hit my stride with Godot's scenes. For my entities within the game, I've been making 'components'. These components can be attached to provide functions or behaviour to an object. This is similar to Unity's GameObject and script system, and how you can attach multiple scripts to a GameObject. </p>

<p>Below is an example of an enemy prototype I have created in my game:</p>

![EnemyScene](/assets/images/2022_01_13-GodotScene.png)

<p>Each of these components can hold state, used to call functions and/or communicate with other components. Their logic is self-contained and can be easily attached to and removed from objects. Dependency Injection is used where components need to access other component's state or connect to their signals.</p>

<p>Because of Godot's scene system, I am also able to attach more than just scripts to these components. Because each scene can be made up of any nodes, I am able to use anything to create the function that the main component will provide. For example, some components contain timers to modify how long they last.</p>

