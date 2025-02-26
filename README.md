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

1. Download & Drag Contents to game folder: https://github.com/ThirteenAG/WidescreenFixesPack/releases
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
### Far Cry 4 [Weapon FOV, and High Core Count CPU Crash Fix]
1. Download: https://www.nexusmods.com/farcry4/mods/61?tab=files&file_id=261
<a href="https://github.com/KowabungaOfficial/Linux-Game-Fix-Index/releases/download/GameModBackups/FarCry4ModBackup.tar.gz">`(Backup)`</a>

2. Drag and Drop patch_hd.dat and patch_hd.fat into "data_win32" folder

3. Environment Variable _(Can Be Used For Heroic/Lutris/Steam)_:
```
PROTON_CPU_TOPOLOGY=8
```

Work in progess, will update soon :) Fallout 3, Fallout New Vegas, and more properly running at high fps on linux.

Fixes\QOL Improvements For Windows Games on Linux. FPS Fixes, FOV Fixes, Post Processing Removal etc.
