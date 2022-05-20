## Introduction
This repository is for reproducing my [stackoverflow question](https://stackoverflow.com/questions/72299376/the-hydroelastic-contact-does-not-give-expected-contact-surface/72307178#72307178).

## How to reproduce
All the related code is in the `error_reproduce.ipynb`. To reproduce the error, you just need to open the `Drake Visualizer` first and then run the cells in `error_reproduce.ipynb` in sequence. 

## Other things
* `init_q_left` is the start position for the `iiwa` robot
* `model/` contains the hole's model, including the `mesh` and `urdf` files
* In the simulation, I firstly command a vertical downward velocity for the peg to make contact with the hole surface and then command a vertical downward force at the end of peg. This applied force locates at the edge of the peg's end and points into the hole's surface (not points into the hollow hole). Since the hole's surface should be able to counteract this force, the peg shouldn't tilt much.