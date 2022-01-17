---
layout: post
title:  "Near Infinite, Procedural Terrain"
category: university
---
<img src="/assets/images/procedural-terrain/terrain.png" alt="" width="100%" height="500px"/>

In the third year of my university degree, for my dissertation I decided to investigate procedural generation. For my dissertation, I used Unity to create a tool where I could generate terrain procedurally, and then expanded this so that terrain is generated at run-time on a near-infinite level as the user flies around the terrain. I then used this tool to compare two different noise generation algorithms, Perlin Noise and OpenSimplex noise.

<img src="/assets/images/procedural-terrain/terrain-top-down.png" alt="" width="100%" height="500px"/>
<img src="/assets/images/procedural-terrain/coordinate-system.png" alt="" class="cover"/>

<img src="/assets/images/procedural-terrain/shader-shading.png" alt="" class="cover"/>

<img src="/assets/images/procedural-terrain/level-of-detail.png" alt="" class="cover"/>

I created a custom shader in Unity that would texture the terrain based on the height of it, and how steep it was.

