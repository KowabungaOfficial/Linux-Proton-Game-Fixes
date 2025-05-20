# Linux Proton Game Fixes

> [!IMPORTANT] 
> **Config File Locations**
>
> <details><summary>Game Launcher Config Location</summary>
>
> Heroic Config Location (For Stuff like Engine.ini etc):
>
> `/home/"YOUR USERNAME GOES HERE"/Games/Heroic/Prefixes/default/"Name Of Game"/pfx/drive_c/users/steamuser/`
> 
> Steam Config Location (For Stuff like Engine.ini etc):
>
> `/SteamLibrary/steamapps/compatdata/"THE GAMES ID NUMBER GOES HERE"/pfx/drive_c/users/steamuser/`
</details>

> [!IMPORTANT]
> **Steam Proton Lag/Stutter/FPS Drop Fix**
>
> **(Lag/Stutter/FPS Drop Caused When Moving Mouse After 20-40 Minutes)**
> 
> Add `LD_PRELOAD="" %command%` to all games in the launch options
>
> Fix Is Mentioned Here:
> [SheMelody](https://github.com/ValveSoftware/steam-for-linux/issues/11446#issuecomment-2467785054)

### Vampyr [FPS, QOL, and High Core Count CPU Crash Fix]

1. Play game first then exit, then edit "engine.ini" for the game and add this to end of file:

```
[SystemSettings]
r.Tonemapper.Quality=0
r.LensFlareQuality=0
r.SceneColorFringeQuality=0
r.LensDOF=0
r.KernelDOF=0
r.GaussDOF=0
r.FilmGrain=0
r.Distortion=0
r.VolumetricFog=0
r.EyeAdaptation=0
r.AutomaticExposure=0
r.Bloom=0
r.BloomQuality=0
r.LightShafts=0
r.DepthOfFieldQuality=0
r.DepthOfField=0
r.DefaultFeature.MotionBlur=0
r.MotionBlur=0
r.MotionBlur.Max=0
r.MotionBlurQuality=0
r.PostProcessOutline=0
r.CharacterOutline=0

[/script/engine.engine]
bSmoothFrameRate=false

[/Script/Engine.LocalPlayer]
AspectRatioAxisConstraint=AspectRatio_MaintainYFOV
```

2. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=8
```
----------------------------------------------------------------
### Ultimate Spider-Man [FPS, FOV, PS5 Control Scheme, and Widescreen Fix]

1. Download & Drag Contents to game folder: <a href="https://github.com/ThirteenAG/WidescreenFixesPack/releases/tag/usm">ThirteenAG Widescreen Fix Mod</a>
<a href="https://github.com/KowabungaOfficial/Linux-Proton-Game-Fixes/releases/download/GameModBackups/UltimateSpiderManWidescreenFixModBackup.tar.gz">`(Backup)`</a>

2. Play game in Heroic or Lutris, change settings to what you prefer then exit game

3. Then edit "UltimateSpiderMan.WidescreenFix.ini" to your liking

4. Use winetricks to include dsound (For heroic you right click game, then under wine section click winetricks)


Control Scheme For PS5 Dualsense Controller:

<img style="width: 450px; height: 298px;" src="https://kowabungaofficial.github.io/Linux-Proton-Game-Fixes/QOLPictures/UltimateSpider-Man_PS5ControllerScheme.png">

---------------------------------------------------------------
### Far Cry 3 [High Core Count CPU Crash Fix]

1. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=4
```
---------------------------------------------------------------
### Far Cry 4 [Viewmodel FOV, and High Core Count CPU Crash Fix]
1. Download: <a href="https://www.nexusmods.com/farcry4/mods/61?tab=files&file_id=261">Schrotflinte12 Viewmodel Fov Mod</a>
<a href="https://github.com/KowabungaOfficial/Linux-Proton-Game-Fixes/releases/download/GameModBackups/FarCry4ModBackup.tar.gz">`(Backup)`</a>

2. Drag and Drop patch_hd.dat and patch_hd.fat into "data_win32" folder

3. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=8
```
---------------------------------------------------------------
### Mass Effect Legendary Edition [QOL, and Game Fix]
1. Add Game Arguments: `-NoHomeDir -SeekFreeLoadingPCConsole`

2. Play with "MassEffectLauncher.exe"

3. (Not Required, but can fix issues) If using another version of game make sure to "add game" and "run installer first" to install the game.
---------------------------------------------------------------
### The Beginners Guide [High Core Count CPU Crash Fix]

1. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=4
```
---------------------------------------------------------------
### The Stanley Parable [High Core Count CPU Crash Fix, and Game Fix]

1. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=8
```
2. If you have a folder named "thestanleyparable" in your game folder rename it to "stanley"
---------------------------------------------------------------
### Bioshock Remastered [Blurry Texture Fix]

1. Disable fsync and esync for game in heroic/lutris.
---------------------------------------------------------------
### Bioshock 2 Remastered [Blurry Texture Fix]

1. Disable fsync and esync for game in heroic/lutris.
---------------------------------------------------------------
### Bioshock Infinite [Blurry Texture Caused By Goverlay Bug Fix] 

1. In Goverlay go to the Performance tab set "Mip-map LoD bias" to "0" (Keep at 0 for all games as well) <a href="https://github.com/doitsujin/dxvk/issues/4571">`Mentioned Here`</a>

- To See Difference Look At The Hat On The Coat Hanger

| Negative Value | (0) Positive Value |
|--------|-------|
| ![Before](https://github.com/KowabungaOfficial/Linux-Proton-Game-Fixes/blob/main/QOLPictures/mnsvleesbsckinfte1.jpg) | ![After](https://github.com/KowabungaOfficial/Linux-Proton-Game-Fixes/blob/main/QOLPictures/zerobshckifinte1.jpg) |

---------------------------------------------------------------
### Spider-Man: Web Of Shadows [Crash Fix and FPS Fix]

1. Use winetricks to include msxml3, msxml6, and vcrun2005

(For heroic you right click game, then under wine section click winetricks)

3. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=4
```

---------------------------------------------------------------
### Xenia Manager (Xenia Canary) [Black Screen Fix] Gears Of War 2, 3, Judgement

1. In linux command line paste this and hit enter:
```
sudo sysctl net.ipv4.ip_unprivileged_port_start=0
```

2. Go inside your xenia folder and open xenia-canary.config.toml.file
Find the line that says lunch_module=""
Input default_mp.xex in between "" marks and save

Example: lunch_module="default_mp.xex"

> [!IMPORTANT]
> Number 1 Has To Be Done Everytime The Kernel Is Updated

---------------------------------------------------------------
### Xenia Manager (Xenia Canary) [Graphics Device Lost Fix] Gears Of War 2, 3, Judgement, & More
1. Set "Queue Priority" to Normal
2. Set "Scribble Heap" to on
3. Make sure "Break On Unimplemented Instructions" is set to off

```
If All Else Fails:
Set "Readback Resolve" to on
This will impact performance though
```
---------------------------------------------------------------

Work in progess, will update soon :) Fallout 3, Fallout New Vegas, and more properly running at high fps on linux.

Fixes\QOL Improvements For Windows Games on Linux. FPS Fixes, FOV Fixes, Post Processing Removal etc.
