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

- **Vampyr** [FPS, QOL, and High Core Count Cpu Crash Fix]

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

Work in progess, will update soon :) Fallout 3, Fallout New Vegas, and more properly running at high fps on linux.

Fixes\QOL Improvements For Windows Games on Linux. FPS Fixes, FOV Fixes, Post Processing Removal etc.
