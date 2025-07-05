---
# these are required
title: Intro to GPU Occlusion
urls:
    - https://youtu.be/gCPgpvF1rUA?si=Ydxe1aXfA1wYghVp
authors:
  - Leon Brands
year: 2024
tags:
  - Optimization
  - GPU
  - Culling
conference: Graphics programming conference
---

The presentation talks about using as much GPU occlusion culling as possible to reduce drawing in heavily dynamic games.

* The previous frame's depth buffer is projected to cull objects in this frame early
* A depth pre-pass is used
* An HZBuffer is used to optimize depth testing
* Limitations are discussed with artifacts arising from the previous frame's data, and artifacts when moving through objects
* Many false positives are encountered when culling, so objects are rendered if they "might" be seen. Rendering these extra objects does not have much impact on performance and is greatly favoured over causing rendering artifacts.
