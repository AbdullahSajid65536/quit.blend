# quit.blend

### A default cube has gone rogue after a failed attempt to delete a recoverable project on your hard drive. It has now consumed the delete button and you are left with very limited options to crack it down. 

<img width="1537" height="1005" alt="image" src="https://github.com/user-attachments/assets/6b4afd20-25f6-4a75-8b57-a53238499980" />

## Gameplay:
The core gameplay loop features an old-school pokemon style turn based combat where you must defeat the default cube without your low budget Nvidia GPU running OOM in the process. It uses RNG mechanics to transact damage between both parties. 

You have a GPU usage stat (essentially an inverted hp bar) and a VRAM counter with 3 different actions that you can take.

### Decimate: 
You apply linear damage to the cube by manually decimating it and this uses no additional VRAM.

### Recompute:
Essentially your heal button. You relinquish GPU cores by refreshing the scene and sideloading the work to the CPU, but your memory slowly fills up due to a leak. Cost: 1MB of VRAM

### Remesh:
You overhaul the entire mesh by running an expensive remesh algorithm. In an ideal circumstance this can effectively halve the current number of verts that the cube has given a good roll. Cost: 48MB of VRAM. 

## Phase 1: 
The cube is relatively well behaved. It can inflict anywhere between 1 to 32% GPU usage per attack. Use recompute to restabilize when necessary. Your GPU bar is color coded to indicate an appropriate level of risk from this phase's standpoint. 

## Phase 2:
```[Scene.001]: bpydata: ???? is a corrupted data block. Proceed with caution.```

Following enough reduction operations, the cube has made the entire blender project buggy. Expect higher GPU usage infliction and tread lightly (there is also an unfair surprise if you are unlucky with a particular roll :D).

Good luck at euthanizing the default cube.

<img width="1038" height="778" alt="image" src="https://github.com/user-attachments/assets/de53ef8e-2c6d-4029-88c7-990691c35415" />


