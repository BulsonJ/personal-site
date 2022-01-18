---
layout: post
title:  "Why I Love Godot's Scenes"
category: blog
---
<p>For just under a year now, I have been using Godot. Over that time, I've gained a lot of familarity with it. While working with it, I've grown to love using Godot's scene system to create my games. It allows for a lot of flexibility and modularity.</p>

<p>While making some prototypes with Godot, I feel like I've hit my stride with the scene system. Previously, I had tried using lots of hardcoded logic and inheritance to allow for code reusability, but I found it tricky to work with. So, currently for the prototype I have been creating I've been making scenes be much more flexible and allow for more reusability. For the majority of these scenes within my prototype, I have called them 'components' as they are the building blocks behind a lot of my entities. These components can be attached to provide functions or behaviour to an object. This is similar to Unity's GameObject and script system, and how you can attach multiple scripts to a GameObject. </p>

<p>Below is an example of an enemy prototype I have created in my game:</p>

![EnemyScene](/assets/images/2022_01_13-GodotScene.png)

<p>Each of these components can hold state, used to call functions and/or communicate with other components. Their logic is self-contained and can be easily attached to and removed from objects. Dependency Injection is used where components need to access other component's state or connect to their signals. However, I love that I can also attach anything to any of these scenes, and it is all abstracted away in a single node that I can access from wherever I place the component.</p>


