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

1. Download & Drag Contents to game folder: <a href="https://github.com/ThirteenAG/WidescreenFixesPack/releases">ThirteenAG Widescreen Fix Mod</a>
<a href="https://github.com/KowabungaOfficial/Linux-Game-Fix-Index/releases/download/GameModBackups/UltimateSpiderManWidescreenFixModBackup.tar.gz">`(Backup)`</a>

2. Play game in Heroic or Lutris, change settings to what you prefer then exit game

3. Then edit "UltimateSpiderMan.WidescreenFix.ini" to your liking

4. Use winetricks to include dsound (For heroic you right click game, then under wine section click winetricks)


Control Scheme For PS5 Dualsense Controller:

<img style="width: 450px; height: 298px;" src="https://kowabungaofficial.github.io/Linux-Game-Fix-Index/QOLPictures/UltimateSpider-Man_PS5ControllerScheme.png">

---------------------------------------------------------------
### Far Cry 3 [High Core Count CPU Crash Fix]

1. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=4
```
---------------------------------------------------------------
### Far Cry 4 [Viewmodel FOV, and High Core Count CPU Crash Fix]
1. Download: <a href="https://www.nexusmods.com/farcry4/mods/61?tab=files&file_id=261">Schrotflinte12 Viewmodel Fov Mod</a>
<a href="https://github.com/KowabungaOfficial/Linux-Game-Fix-Index/releases/download/GameModBackups/FarCry4ModBackup.tar.gz">`(Backup)`</a>

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

1. In Goverlay in the Performance tab make sure "Mip-map LoD bias" is at "0" (Keep it that way for all games as well)

- ### (Worst) Mip-map LoD bias (Negative Values)
<img style="width: 640px; height: 480px;" src="https://kowabungaofficial.github.io/Linux-Game-Fix-Index/QOLPictures/negativevaluesbioshockinfinite.jpg">

- ### (Best) Mip-map LoD bias (At 0)
<img style="width: 640px; height: 480px;" src="https://kowabungaofficial.github.io/Linux-Game-Fix-Index/QOLPictures/0valuebioshockinfinite.jpg">

Work in progess, will update soon :) Fallout 3, Fallout New Vegas, and more properly running at high fps on linux.

Fixes\QOL Improvements For Windows Games on Linux. FPS Fixes, FOV Fixes, Post Processing Removal etc.
