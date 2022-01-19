---
layout: post
title:  "Near Infinite, Procedural Terrain"
category: university
---
<img src="/assets/images/procedural-terrain/terrain.png" alt="" width="100%" height="500px"/>

In the third year of my university degree, for my dissertation I decided to investigate procedural generation. For my dissertation, I used Unity to create a tool where I could generate terrain procedurally, and then expanded this so that terrain is generated at run-time on a near-infinite level as the user flies around the terrain. I then used this tool to compare two different noise generation algorithms, Perlin Noise and OpenSimplex noise.

<img src="/assets/images/procedural-terrain/terrain-top-down.png" alt="" width="100%" height="500px"/>

The terrain is broken up into chunks. Each chunk is 255 vertices across. The noise to generate the height map has a variety of parameters to control it, and I even layered into two seperate heightmaps. The first height map had larger, more smooth features to shape the overall look of the landscape. Then, a second layer of noise was generated which had a lot of smaller detail. These combined together gave great results.

<img src="/assets/images/procedural-terrain/coordinate-system.png" alt="" class="cover"/>

To create the "infinite" system, I generated chunks on the fly. Chunks only close to the camera were generated and once the player flew far away enough, chunks were automatically hidden.

<img src="/assets/images/procedural-terrain/shader-shading.png" alt="" class="cover"/>

Because the terrain was procedurally generated, I could not texture it before hand. I created a custom shader in Unity that used a variety of textures to add sand, grass, rock etc to the terrain. They are then blended together based on the height of the terrain, and how steep it is. 

<img src="/assets/images/procedural-terrain/level-of-detail.png" alt="" class="cover"/>

Chunks also had a level of detail system, so that more chunks could be on screen at one time. The further away the chunk was, the lower resolution the mesh used to display it.

