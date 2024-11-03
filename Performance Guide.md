![](https://raw.githubusercontent.com/TwistedModding/TwistedModdingLists/refs/heads/main/Twisted%20Skyrim%20logo.webp)

<p align="center">
  <a href="https://www.nexusmods.com/skyrimspecialedition/mods/87820](https://www.nexusmods.com/skyrimspecialedition/mods/132034">Nexus</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/README.md">Installation</a> |
  <a href="https://loadorderlibrary.com/lists/twisted-skyrim">Modlist</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/FAQ.md">FAQ</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/Performance%20Guide.md">Performance Guide</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/GAMEPLAY%20GUIDE.md">Gameplay Guide</a>
</p>

---

# Performance Guide

**Although this is made to be as clear as possible, if you aren't a tech savvy person or have never modded before this probably isn't for you. I won't babysit people step by step on what to do as the guide is pretty much as clear as it possibly can be.**

### Attention

**Modlist Support: [Twisted Skyrim](https://discord.gg/jJ3xH5b9Jh)**

**Any deviation from this guide counts as an authorized modification of the list and thus breaks rule 11. Please seek help using the #changes-additions-rule-11 channel on the discord for further help.**

**Most of these steps will need to be done after every update, I recommend backing up any changes so you can just copy and paste the files over the new update.**

### Contents
- [Attention](#Attention)
- [Modifying Game INIs](#Modifying-Game-INIs)
- [Disabling your ENB](#Disabling-ENB-OPTIONAL)
- [LODS](#LODS)
  - [xLODGEN](#xLODGEn)
  - [TexGen](#TexGen)
  - [DynDOLOD](#DynDOLOD)
- [VRAMr](#VRAMr)

### Modifying Game INIs
**MO2 uses a profile system, which means any ini edits you make will only effect that profile you are currently on, make sure you are on the desired MO2 profile before continuing.**
**MAKE SURE MO2 IS CURRENTLY CLOSED**

1. Open Twisted Skyrim's mo2 directory. Mine is located here: `E:\Twisted Skyrim`
2. Open the `Tools` folder.
3. Open the `BethINI Standalone` folder.
4. Open `BethINI.exe` **MAKE SURE MO2 IS CLOSED.**
5. Ignore any updates BethINI prompts you with.
6. Select the `Setup` tab.
7. Ensure the INI path is set properly, this will either be `\profiles\Twisted Skyrim\` or `\profiles\Twisted Skyrim SFW` depending on the profile you play on. For me it is `\profiles\Twisted Skyrim PERSONAL\` Since I have a personal version of my list I play on.
8. Select the `Basic` tab.
9. Select the `Medium` preset & tick `Recommended Tweaks` afterwards.
10. Make sure `Borderless` is ticked & `64-Bit Render Targets` **Antialiasing set to TAA is recommended but not required.**
11. Switch to the `Detail` tab
12. Tick all the boxes under the `Water` section (Reflect trees, reflect objects, etc)
13. `Godrays` to low
14. `Particles` 6000 minimum
15. `Decals`, `Depth of Field`, & `Anamorphic Lens Flare` Enabled. **ENABLE REGULAR LENS FLARE IF YOU DON'T PLAY WITH ENB
16. `Shadow resolution` 2048 or lower, I don't recommend going lower than 2048
17. `Shadow bias` 0.15
18. `Detailed Draw Distance` 2000 or lower, I don't recommend lower than 2000.
19. `Exterior Draw Distance` 6000 or lower, I don't recommend lower than 6000.
20. Tick `Tree Shadows` & `Land Shadows`
21. Untick `Ambient Occlusion` **LEAVE ENABLED IF YOU DON'T USE ENB**
22. Tick `Screen Space Reflections`
23. Set the `Reflection Divider` from anything between 1-9. 1 Looking the best, 9 the worst. Technically can go up to 18 if you desperately need performance, but not recommended to go beyond 9.
24. `Object Fade` 15
25. `Actor Fade` 12
26. `Item Fade` 4.5
27. `Light Fade` 30720
28. `Flickering Light` 8192
29. `Object Detail Fade` Ultra
30. `Basic` tab
31. Save and Exit

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
1. Navigate to the `Stock Game` folder. Mine is here: `E:\Twisted Skyrim\Stock Game`
2. Change `d3d11.dll` to `d3d11.dll.bak` **This will need to be done every update**

### Tintmask Resolution
1. Go to `E:\Twisted Skyrim\mods\Vanilla Warpaints Absolution\SKSE`
2. Open `SKSE.ini`
3. Change `iTintTextureResolution=4096` to `iTintTextureResolution=2048` *Note, this can go lower, if you really need the performance drop it to as low as 512(vanilla)
4. Ctrl+S to save
5. Exit

# LODS 

### xLODGEN
1. Download [xLODGEN](https://mega.nz/file/NF5jQbjR#GZHwX_NpFtR-A4AM3DcnXW9jHnZAhLJMsAm3JDB-VWU)
2. Extract the folder in the zip called `xLODGen` to `E:\Twisted Skyrim\tools`, you should now have a directory like this `E:\Twisted Skyrim\tools\xLODGen`
3. Create a new folder in `E:\Twisted Skyrim\tools` called `ACMOS - Road Generator`.
4. Download [ACMOS Road Generator](https://www.nexusmods.com/skyrimspecialedition/mods/79205?tab=files)
5. Extract it to the newly created folder `E:\Twisted Skyrim\tools\ACMOS Road Generator`
6. MO2 should already have xLODGen added as an executable, if it doesn't launch MO2, select the drop down, select `Edit` and a windows should pop up. Click the `+` sign `add from file` and look for your xLODGen.exe and select it. Hit apply and ok.
7. Regardless of whether its added or not, select the drop down again in MO2, in the `Arguments` section on xLODGen, make sure it looks like this: `-SSE -o:"C:\Users\jlbom\Desktop\xlodgen"` changing the given directory to match a similar place on your computer OUTSIDE of MO2. I recommend keeping it at your desktop.
8. Hit `apply` and `ok`.
9. Locate the mod `xLODGen Output` open it by holding CTRL and double clicking it. Delete the contents `Meshes` & `Textures`
10. Do the same for the mods `Road output` `TexGen Output` & `DynDOLOD Output`
11. Enable the mod `xLODGen Resource - SSE Terrain Tamriel` if its not present in the load order, download from [here](https://www.nexusmods.com/skyrimspecialedition/mods/54680?tab=files) select the `SSE Terrain Tamriel Extend` version to download, install and enable it within MO2.
12. Make sure the plugin `SSE-Terrain-Tamriel-Extend.esm` is enabled in the right pane of MO2 (plugins list).
13. Launch xLODGen within MO2
14. Copy the settings below EXACTLY,
    
<img width="451" alt="xLODGenx64_gd9DQvWwwL" src="https://github.com/user-attachments/assets/83b61ae7-8eaf-4891-889a-c004abe17d37">
<img width="451" alt="xLODGenx64_XVMmTC8bnB" src="https://github.com/user-attachments/assets/cb7dd710-fda0-4334-ae62-0de79783e861">
<img width="451" alt="xLODGenx64_IgrBRa82Rs" src="https://github.com/user-attachments/assets/5f5030ef-7c27-42e5-bde2-a80a8a700528">
<img width="451" alt="xLODGenx64_avCy5vKUik" src="https://github.com/user-attachments/assets/c873e5cc-813a-4491-8607-b200b25b8e54">

14. Select `Generate` on the bottom of the screen and wait for it to finish.
15. Once finished, the output will be where ever you set it in step #7. Locate and open that folder, Cut (ctrl x) and paste it (ctrl V) into the mod `xLODGen output` within mo2. That mod should now look like this:

<img width="414" alt="explorer_ymJso5MJwm" src="https://github.com/user-attachments/assets/5b446c3f-3539-411b-abb3-f55a6f5734cc">

16. Go to where you installed ACMOS, for me `E:\Twisted Skyrim\tools\ACMOS Road Generator`.
17. Open `ACMOS Road Generator.exe`
18. `Select Roads` should be `Paths Only`
19. Path to `LOD` should be `E:\Twisted Skyrim\mods\xLODGen Output`
20. Path to `Output Path` should be `E:\Twisted Skyrim\mods\Road Output`
21. `Generate`
22. Wait for it to finish, make sure to NOT zip it after it's done.
23. Disable the mod `xLODGen Resource - SSE Terrain Tamriel`

### TexGen
1. Go to [DynDOLODs mod page](https://www.nexusmods.com/skyrimspecialedition/mods/68518?tab=files) click manual download and extract the contents to whatever drive you want. **Make sure that it is the root directory of that drive such as C:/ or D:/**
2. Where ever you extracted DynDOLOD, for me `C:/DynDOLOD`, navigate to `DynDOLOD_SSE.ini`. Mine is found here `"C:\Dyndolod\Edit Scripts\DynDOLOD\DynDOLOD_SSE.ini"`.
3. Open the file
4. Set `Expert=0` to `Expert=1` & `Level32=0` to `Level32=1` & `TreeLODComplexAtlas=0` to `TreeLODComplexAtlas=1`
5. Save the file with ctrl+s and close it.
6. Open MO2
7. Select the dropdown menu
8. Select `Edit`
9. Look for TexGen, select it and where it says `Binary` make sure that matches to where you installed TexGen, for me `C:\Dyndolod\TexGenx64.exe`
10. Look for DynDOLOD, select it and where it says `Binary` make sure that matches to where you installed DynDOLOD, for me `C:\Dyndolod\DynDOLODx64.exe`
11. Make sure the `Arguements` for both programs have `-SSE`
12. Apply and Ok.
13. Launch TexGen within MO2
14. Make sure it matches mine **EXACTLY**

    <img width="396" alt="TexGenx64_Qtx353ZB5k" src="https://github.com/user-attachments/assets/781efad2-3149-441b-940c-2779739ed226">

15. Click start and wait for it to finish.
16. Go to your output folder, for me `C:\Dyndolod\TexGen_Output`
17. Cut and paste the contents from there, to `E:\Twisted Skyrim\mods\TexGen Output`

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


# VRAMr
A tool that I've never personally used, but have heard it works fairly well.
[VRAMr](https://www.nexusmods.com/skyrimspecialedition/mods/90557)

VRAMr includes a user guide on the mod page, you should direct any and all questions towards the mod author on how to use it. Using this tool is unofficially supported by me(TwistedModding) and therefore I will not help you get it up and running. 

With that said, it can take VRAM usage down as much as 10 gbs and make the list playable on much lower end hardware. It can take several hours and will signifcantly increase the amount of space needed for the list since (i think) outputs all textures to a new mod instead of replacing existing ones (which is a good thing, just takes up space obviously). 

I'd suggest only running this if the rest of the performance guide did not do a good enough job at making the list playable on your hardware.
