# Linux Game Fix Index

- **Vampyr** [FPS and High Core Count Cpu Crash Fix]

Edit the engine.ini file for the game and add this to end of file:

```
[/script/engine.engine]
bSmoothFrameRate=false
```

Environment Variable
```
PROTON_CPU_TOPOLOGY=8
```

Work in progess, will update soon :) Fallout 3, Fallout New Vegas, and more properly running at high fps on linux.

Fixes\QOL Improvements For Windows Games on Linux. FPS Fixes, FOV Fixes, Post Processing Removal etc.
