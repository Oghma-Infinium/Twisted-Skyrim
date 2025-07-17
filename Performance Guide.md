![](https://raw.githubusercontent.com/Oghma-Infinium/Twisted-Skyrim/refs/heads/main/Twisted%20Skyrim%20Logo%20(1).webp)

<p align="center">
  <a href="https://www.nexusmods.com/skyrimspecialedition/mods/87820](https://www.nexusmods.com/skyrimspecialedition/mods/132034">Nexus</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/README.md">Installation</a> |
  <a href="https://loadorderlibrary.com/lists/twisted-skyrim-2">Modlist</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/FAQ.md">FAQ</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/CHANGELOG.md">Changelog</a> |
  Performance Guide |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/GAMEPLAY%20GUIDE.md">Gameplay Guide</a>
</p>

---

# Performance Guide

## Contents
- [Performance and YOU](#performance-and-you)
- [Attention](#Attention)
- [Modifying Game INIs](#Modifying-Game-INIs)
- [Disabling your ENB](#Disabling-ENB-OPTIONAL)
- [ParallaxGen](#Preface-LODs)
- [LODS](#LODS)
  - [xLODGEN](#xLODGEn)
  - [TexGen](#TexGen)
  - [DynDOLOD](#DynDOLOD)
- [VRAMr](#VRAMr)
- [Upscaler Info](#Upscalers)

**Although this is made to be as clear as possible, if you aren't a tech savvy person or have never modded before this probably isn't for you. I won't babysit people step by step on what to do as the guide is pretty much as clear as it possibly can be.**

## Performance and YOU

I suggest getting an overlay that lets you see GPU & RAM usage, CPU usage, despite what people think does NOT matter for gaming. If your GPU usage sits at or above 98% consistently, then a GPU upgrade would help the most. If your GPU usage sits consistently sits BELOW ~98% then a CPU upgrade would benefit you, the ONLY CPUs I will recommend are the x3D chips from AMD (5800x3d, 7800x3d & 9800x3d). If your RAM is always filled, or almost always filled, a RAM upgrade would likely reduce stuttering

### Attention

**Modlist Support: [Twisted Skyrim](https://discord.gg/wakingdreams)**

**Any deviation from this guide counts as an unauthorized modification of the list and thus breaks rule 11. Please seek help using the #changes-additions-rule-11 channel on the discord for further help.**

**Most of these steps will need to be done after every update, I recommend backing up any changes so you can just copy and paste the files over the new update.**

### Modifying Game INIs
**MO2 uses a profile system, which means any ini edits you make will only effect that profile you are currently on, make sure you are on the desired MO2 profile before continuing.**
**MAKE SURE MO2 IS CURRENTLY CLOSED**

1. Open Twisted Skyrim's mo2 directory. Mine is located here: `E:\Twisted Skyrim`
2. Open the `Tools` folder.
3. Open the `BethINI Standalone` folder.
4. Open `BethINI.exe` **MAKE SURE MO2 IS CLOSED.**
5. Ignore any updates BethINI prompts you with.
6. Select the `Edit` dropdown menu, and select `Setup`.
7. Ensure the INI path is set properly, this will either be `\profiles\Twisted Skyrim\` or `\profiles\Twisted Skyrim SFW` depending on the profile you play on. For me it is `\profiles\Twisted Skyrim PERSONAL\` Since I have a personal version of my list I play on.
8. Select the `Basic` tab.
9. Select the `Medium` preset & press the ` Apply Recommended Tweaks` button afterwards.
10. Make sure `Borderless` is ticked & `64-Bit Render Targets` **Antialiasing set to TAA is recommended but not required.**
11. Select the `Shadows` tab.
12. Shadow bias `0.15`, Shadow filtering `4.0`.
13. Detailed draw distance default is `2800`, I would not recommend going lower than `2000`
14. Exterior draw distance default is `10000`, I would not recommend going lower than `6000`
15. Make sure the ambient occlusion checkbox is unchecked. **You can leave this enabled if you disable ENB's ambient occlusion for more performance.** *This is recommended if you care more about performance than visuals*
16. Go to the `Visuals` tab.
17. Set godrays to `low`.
18. Set particles to no lower than `6000`.
19. Keep depth of field `on`, otherwise it will break the underwater shader.
20. Set SSR Resolution Divider to 9, not recommended to go lower. *You can disable SSR all together by disabling the checkbox, however, it will make the game look a lot more flat.*
21. Select the file dropdown menu and hit `save`.
22. Close BethINI.

### Modifying ENB
1. Navigate to the `Stock Game` folder. Mine is here: `E:\Twisted Skyrim\Stock Game`
2. Open `enbseries.ini`
3. Set lines 40-45 to false. `EnableComplexParallax` `EnableComplexParallaxShadows` `EnableComplexTerrainParallax` `EnableComplexTerrainParallaxShadows` `EnableTerrainBlending=true` `EnableComplexMaterial` should all be false.
4. Ctrl+F to search for `SSAO_SSIL`
5. Change `ResolutionScale` to 0.35
6. Change `SourceTexturesScale` to 0.5
7. `Ctrl+S` to save.
8. Close the file.

   **OPTIONAL**
   Set `EnableAmbientOcclusion` to false as well, this will give the biggest performance boost without actually disabling ENB. Make sure to enable game ambient occlusion as said in the previous step [Modifying Game INIs](#Modifying-Game-INIs)

**Launch your game after these 2 steps to see if performance is satisfactory before continuing.** See [Disabling ENB OPTIONAL](#Disabling-ENB-OPTIONAL)

### Disabling ENB *OPTIONAL*
**This list heavily relies on ENB features for certain effects, it is NOT recommended to disable it completely.**
1. Navigate to the `Stock Game` folder. Mine is here: `E:\Twisted Skyrim\Stock Game`
2. Change `d3d11.dll` to `d3d11.dll.bak` **This will need to be done every update**

### Tintmask Resolution
1. Go to `E:\Twisted Skyrim\mods\Vanilla Warpaints Absolution\SKSE`
2. Open `SKSE.ini`
3. Change `iTintTextureResolution=4096` to `iTintTextureResolution=2048` *Note, this can go lower, if you really need the performance drop it to as low as 512(vanilla)
4. Ctrl+S to save
5. Exit

# PREFACE LODs

### Deleting Outputs
1. Locate the mod `ParallaxGen Ouput` open it by holding CTRL and double clicking it. Delete everything in the folder.
2. Do the same for the mods `xLODGEN Output` `Road Output` `TexGen Output` & `DynDOLOD Output`
3. **Disable** the mod `ParallaxGen Ouput` after deleting its contents

### Generating ParallaxGen
1. Launch `ParallaxGen` from the dropdown menu in MO2, once opened select `Start Patching`
2. Ignore any warnings/errors and once its done select any key on your keyboard to close the command prompt
3. Reenable `ParallaxGen Ouput` and make sure its plugins are enabled and loaded last in the plugins tab of MO2

# LODS 

### xLODGEN
1. Select the drop down menu in MO2, select `edit` in the `Arguments` section on xLODGen, make sure it looks like this: `-SSE -o:"C:\Users\jlbom\Desktop\xlodgen"` changing the given directory to match a similar place on your computer OUTSIDE of MO2. I recommend keeping it at your desktop.
2. Hit `apply` and `ok`.
3. Enable the mod `xLODGen Resource - SSE Terrain Tamriel` if its not present in the load order, download from [here](https://www.nexusmods.com/skyrimspecialedition/mods/54680?tab=files) select the `SSE Terrain Tamriel Extend` version to download, install and enable it within MO2.
4. Make sure the plugin `SSE-Terrain-Tamriel-Extend.esm` is enabled in the right pane of MO2 (plugins list).
5. Launch xLODGen within MO2
6. Copy the settings below EXACTLY,
    
<img width="451" alt="xLODGenx64_gd9DQvWwwL" src="https://github.com/user-attachments/assets/83b61ae7-8eaf-4891-889a-c004abe17d37">
<img width="451" alt="xLODGenx64_XVMmTC8bnB" src="https://github.com/user-attachments/assets/cb7dd710-fda0-4334-ae62-0de79783e861">
<img width="451" alt="xLODGenx64_IgrBRa82Rs" src="https://github.com/user-attachments/assets/5f5030ef-7c27-42e5-bde2-a80a8a700528">
<img width="451" alt="xLODGenx64_avCy5vKUik" src="https://github.com/user-attachments/assets/c873e5cc-813a-4491-8607-b200b25b8e54">

9. Select `Generate` on the bottom of the screen and wait for it to finish.
10. Once finished, the output will be where ever you set it in step #7. Locate and open that folder, Cut (ctrl x) and paste it (ctrl V) into the mod `xLODGen output` within mo2. That mod should now look like this:

<img width="414" alt="explorer_ymJso5MJwm" src="https://github.com/user-attachments/assets/5b446c3f-3539-411b-abb3-f55a6f5734cc">

11. Go to where you installed ACMOS, for me `E:\Twisted Skyrim\tools\ACMOS Road Generator`.
12. Open `ACMOS Road Generator.exe`
13. `Select Roads` should be `Paths Only`
14. Path to `LOD` should be `E:\Twisted Skyrim\mods\xLODGen Output`
15. Path to `Output Path` should be `E:\Twisted Skyrim\mods\Road Output`
16. `Generate`
17. Wait for it to finish, make sure to NOT zip it after it's done.
18. Disable the mod `xLODGen Resource - SSE Terrain Tamriel`

### TexGen
1. Right click `SKSE Ouptut` and select `Open in Explorer`. 
2. Follow this directory `C:\Twisted Skyrim\mods\SKSE Output\SKSE\Plugins\GrassControl.ini`.
3. Open `GrassControl.ini`.
4. Change `DynDOLOD-Grass-Mode = 1` to `DynDOLOD-Grass-Mode = 0`
5. CTRL+S to save, then close.
6. Go to [DynDOLODs mod page](https://www.nexusmods.com/skyrimspecialedition/mods/68518?tab=files) click manual download and extract the contents to whatever drive you want. **Make sure that it is the root directory of that drive such as C:/ or D:/**
7. Where ever you extracted DynDOLOD, for me `C:/DynDOLOD`, navigate to `DynDOLOD_SSE.ini`. Mine is found here `"C:\Dyndolod\Edit Scripts\DynDOLOD\DynDOLOD_SSE.ini"`.
8. Open the file
9. Set `Expert=0` to `Expert=1` & `Level32=0` to `Level32=1` & `TreeLODComplexAtlas=0` to `TreeLODComplexAtlas=1`
10. Save the file with ctrl+s and close it.
11. Open MO2
12. Select the dropdown menu
13. Select `Edit`
14. Look for TexGen, select it and where it says `Binary` make sure that matches to where you installed TexGen, for me `C:\Dyndolod\TexGenx64.exe`
15. Look for DynDOLOD, select it and where it says `Binary` make sure that matches to where you installed DynDOLOD, for me `C:\Dyndolod\DynDOLODx64.exe`
16. Make sure the `Arguements` for both programs have `-SSE`
17. Apply and Ok.
18. Locate the mod `TexGen Output` open it by holding CTRL and double clicking it. Delete everything in this folder.
19. Locate the mod `DynDOLOD Output` open it by holding CTRL and double clicking it. Delete everything in this folder.
20. Launch TexGen within MO2
21. Make sure it matches mine **EXACTLY**

    <img width="396" alt="TexGenx64_Qtx353ZB5k" src="https://github.com/user-attachments/assets/781efad2-3149-441b-940c-2779739ed226">

22. Click start and wait for it to finish.
23. Go to your output folder, for me `C:\Dyndolod\TexGen_Output`
24. Cut and paste the contents from there, to `E:\Twisted Skyrim\mods\TexGen Output`

### DynDOLOD
**MAKE SURE STEPS 2-5 IN THE TEXGEN SECTION ARE COMPLETED BEFORE CONTINUING.**
1. Launch DynDOLOD within MO2
2. Right click the top left box and hit `Select all`
3. Select the `Medium` preset in the top right
4. Scroll all the way down in the section in the middle
5. Double click `tree` and change `LOD Level 32` to Billboard6 from whatever it is.
6. Click `ok`
7. Double click `\` and change `Lod Level 32` to `Level0` from whatever it is.
8. Make sure the rest matches mine EXACTLY
   
<img width="667" alt="DynDOLODx64_TNknkqgsUf" src="https://github.com/user-attachments/assets/9217e1e3-eb3e-4682-8257-272f7a8cbba3">

9. Click ok and wait for it to finish. **If it fails and errors on anything, that means you made unauthorized modifications to the list and I will not help you.**
10. Go to your output folder, for me `C:\Dyndolod\DynDOLOD_Output`
11. Cut and paste the contents from there, to `E:\Twisted Skyrim\mods\DynDOLOD Output`
12. Refresh MO2 by clicking `F5` or just restart MO2
13. Enable the plugins `DynDOLOD.esm`, `DynDOLOD.esp` & `Occlusion.esp`

### Final step
1. Make sure `DynDOLOD.esm` is loaded as late as it can be in the plugins tab of MO2. Mine for reference is loaded right AFTER the `Lux` separator in the plugins tab of MO2.
2. Make sure at the bottom of your load order you have the following plugins: `ParallaxGen.esp` `PG_1.esp` `DynDOLOD.esp` `Occlusion.esp`  <---- **MAKE SURE THEY ARE IN THAT ORDER

# VRAMr

**NOTE** *This tool has been reported to cause crashes when used with this list, before reporting any bugs, please make sure the crash happens without the output enabled.*

A tool that I've never personally used, but have heard it works fairly well.
[VRAMr](https://www.nexusmods.com/skyrimspecialedition/mods/90557)

VRAMr includes a user guide on the mod page, you should direct any and all questions towards the mod author on how to use it. Using this tool is unofficially supported by me(TwistedModding) and therefore I will not help you get it up and running. 

With that said, it can take VRAM usage down as much as 10 gbs and make the list playable on much lower end hardware. It can take several hours and will signifcantly increase the amount of space needed for the list since (i think) outputs all textures to a new mod instead of replacing existing ones (which is a good thing, just takes up space obviously). 

I'd suggest only running this if the rest of the performance guide did not do a good enough job at making the list playable on your hardware.

# Upscalers

**I do not provide any support with upscalers**

Both Puredark's and Doodlum's upscalers have issues of their own that may cause crashes or other oddities when using them in this list, I **DO NOT** recommend using either. You *can* try lossless scaling, but I haven't had amazing luck using it and getting good results in my own game.

