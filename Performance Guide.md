![](https://raw.githubusercontent.com/TwistedModding/TwistedModdingLists/refs/heads/main/Twisted%20Skyrim%20logo.webp)

<p align="center">
  <a href="https://www.nexusmods.com/skyrimspecialedition/mods/87820](https://www.nexusmods.com/skyrimspecialedition/mods/132034">Nexus</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/README.md">Installation</a> |
  <a href="https://loadorderlibrary.com/lists/twisted-skyrim">Modlist</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/FAQ.md">FAQ</a> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="Performance Guide"> |
  <a href="https://github.com/TwistedModding/TwistedModdingLists/blob/main/GAMEPLAY%20GUIDE.md">Gameplay Guide</a>
</p>

---
<p align="center">
 UNDER CONSTRUCTION
</p>

# Performance Guide

### Attention

**Modlist Support: [Twisted Skyrim](https://discord.gg/jJ3xH5b9Jh)**

**Any deviation from this guide counts as an authorized modification of the list and thus breaks rule 11. Please seek help using the #changes-additions-rule-11 channel on the discord for further help.**

**Most of these steps will need to be done after every update, I recommend backing up any changes so you can just copy and paste the files over the new update.**

### Contents
- [Attention](#Attention)
- [Tools](#Tools)
- [Setting the INI](Setting-the-INI)
- [Modifying Game INIs](#Modifying-Game-INIs)
- [Disabling your ENB](#Disabling-ENB-OPTIONAL)

### Tools
Go to [DynDOLODs mod page](https://www.nexusmods.com/skyrimspecialedition/mods/68518?tab=files) click manual download and extract the contents to whatever drive you want. **Make sure that it is the root directory of that drive such as C:/ or D:/**

### Setting the INI
1. Whereever you extracted DynDOLOD, for me `C:/DynDOLOD`, navigate to `DynDOLOD_SSE.ini`. Mine is found here `"C:\Dyndolod\Edit Scripts\DynDOLOD\DynDOLOD_SSE.ini"`.
2. Open the file
3. Set `Expert=0` to `Expert=1` & `Level32=0` to `Level32=1` & `TreeLODComplexAtlas=0` to `TreeLODComplexAtlas=1`
4. Save the file with ctrl+s and close it.

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
23. Set the `Reflection Divider` from anything between 1-9. 1 Looking the best, 9 the worst.
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

# LODS 
<p align="center">
 UNDER CONSTRUCTION
</p>

# VRAMr
A tool that I've never personally used, but have heard it works fairly well.
[VRAMr](https://www.nexusmods.com/skyrimspecialedition/mods/90557)

VRAMr includes a user guide on the mod page, you should direct any and all questions towards the mod author on how to use it. Using this tool is unofficially supported by me(TwistedModding) and therefore I will not help you get it up and running. 

With that said, it can take VRAM usage down as much as 10 gbs and make the list playable on much lower end hardware. It can take several hours and will signifcantly increase the amount of space needed for the list since (i think) outputs all textures to a new mod instead of replacing existing ones (which is a good thing, just takes up space obviously). 

I'd suggest only running this if the rest of the performance guide did not do a good enough job at making the list playable on your hardware.
