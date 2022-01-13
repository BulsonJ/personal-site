---
layout: post
title:  "Godot Component System"
caegory: blog
---
<p>Although my aim was to try to keep components completely unaware of each other, I found it beneficial to code within the components behaviour which I expected to reuse and was not ambigous when connected to other components. For example, if you look at the Health Component:</p>

![Health Component](/assets/images/2022_01_13-GodotHealth.png)

<p>The Health Component is primarily used to hold the health state of something, usually the parent object(in this case, the Enemy). It has functions for setting the current health, max health, and contains signals to tell other objects when the health has changed, there is no health left etc. </p>

<p>However, one common behaviour is that when the entity receives a hit, the damage from that hit will be taken away from the health of that entity. So, instead of having to code that in every entity's main script, I have used dependency injection to allow for communication between components. In this example, the Health Component can have a Hitbox Component attached. In the Health Component's ready() function, it then connects to the hit_taken() signal of the Hitbox Component. If there is no Hitbox Component specified, then the Health component can still be used, just that the predefined behaviour between a health component and a hitbox component will not take place automatically.</p>