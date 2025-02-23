# Linux Game Fix Index

> [!IMPORTANT] 
> **Config File Locations Are As Listed**
> 
> _Heroic Config Location (For Stuff like Engine.ini etc):_
>
> `/home/"YOUR USERNAME GOES HERE"/Games/Heroic/Prefixes/default/"Name Of Game"/pfx/drive_c/users/steamuser/`
>
> _Steam Config Location (For Stuff like Engine.ini etc):_
>
> `/SteamLibrary/steamapps/compatdata/"The Games ID Number"/pfx/drive_c/users/steamuser/`

- **Vampyr** [FPS and High Core Count Cpu Crash Fix]

Play game first then edit engine.ini for the game and add this to end of file:

```
[/script/engine.engine]
bSmoothFrameRate=false
```

Environment Variable:
```
PROTON_CPU_TOPOLOGY=8
```

Work in progess, will update soon :) Fallout 3, Fallout New Vegas, and more properly running at high fps on linux.

Fixes\QOL Improvements For Windows Games on Linux. FPS Fixes, FOV Fixes, Post Processing Removal etc.
