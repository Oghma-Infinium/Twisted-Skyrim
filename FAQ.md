![](https://raw.githubusercontent.com/Oghma-Infinium/Twisted-Skyrim/refs/heads/main/Twisted%20Skyrim%20Logo%20(1).webp)

<p align="center">
  <a href="https://www.nexusmods.com/skyrimspecialedition/mods/87820](https://www.nexusmods.com/skyrimspecialedition/mods/132034">Nexus</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/README.md">Installation</a> |
  <a href="https://loadorderlibrary.com/lists/twisted-skyrim-2">Modlist</a> |
  FAQ |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/Performance%20Guide.md">Performance Guide</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/GAMEPLAY%20GUIDE.md">Gameplay Guide</a>
</p>

---

# FAQ

### Q: Do I have to read this?
> A: No, but if you ask me any question on this document, I will refer you back to here.

### Q: What do I do if my game crashes?
> A: Post the crashlog, found here C:\Users\{USERNAME}\Documents\My Games\Skyrim Special Edition\SKSE, along with any changes done to the MCM or modlist to the [GitHub issues page](https://github.com/Oghma-Infinium/Twisted-Skyrim/issues) or in the [discord support channel](https://discord.com/channels/1008047161281347606/1374528223706349679).

### Q: What is performance like?
> A: Extremely system dependent, see the readme for my specs and recommended specs

### Q: How can I change the resolution?
> A: Open the folder `F:\Twisted Skyrim\mods\SSE Display Tweaks\SKSE\Plugins` open the file `SSEDisplayTweaks.ini` set `BorderlessUpscale=false` to `BorderlessUpscale=true` & change your resolution to the desired.

### Q: What can I do to improve performance?
> A: Follow the _ENTIRE_ [peformance guide](https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/Performance%20Guide.md) This will significantly improve your frames for those who care more about framerate than visuals.

### Q: What mod is it that makes favorited items/potions/quest items show on my character?
> A: [Immersive Equipment Displays](https://www.nexusmods.com/skyrimspecialedition/mods/62001). You can open the menu with `Left Shift+Backspace` to customize what you want to show and what you don't want to show. You can also use IED to determine weapon positioning (if you want weapons to be sheathed on back for example).

### Q: Why do I have two sets of ears?
> A: Go to the `Hair` tab in racemenu, `facial hairs`, then change the slider to `6`.

### Q: I don't like the 3rd person camera stuff, how can I change it?
> A: Open up the MCM look for `smoothcam` and either play around with the settings on the currently selected preset, or try swapping to one of the other presets included.

### Q: How can I change the first person camera settings?
> A: Open the console and type `ic menu`. Alternatively, you can simply disable `Improved Camera` in mo2.

### Q: What mod unpauses the menus? 
> A: `Skyrim Souls RE Updated`, you can tweak its settings in `C:\Twisted Skyrim\mods\Skyrim Souls RE - Updated\SKSE\Plugins\SkyrimSoulsRE.ini`. From here you can modify which menus stay paused or unpaused.

### Q: When do dragons start spawning?  
> A: By default, dragons are set to begin spawning once the player reaches level 10. Dragons do however have set spawns in certain parts of the map, along with dragon burials. Venture carefully.

### Q: I can't find Altano in the Windpeak Inn. / How do I start VIGILANT?  
> A: VIGILANT requires the player be level 25, completion of House of Horrors, and completion of Kindred Judgement (the final quest of Dawnguard DLC).

### Q: What is the Pilgrim skill / How do I access the Pilgrim skill tree?
> A: The Pilgrim skill is added by [Pilgrim - Custom Skills Framework Addon](https://www.nexusmods.com/skyrimspecialedition/mods/93913) and acts as the way to progress the religion mechanic in the list. You can access the skill tree by using the **Pray** power while sneaking.

### Q: How do I set up the quick wheel?
> A: There is extensive documentation on the mod page [here](https://www.nexusmods.com/skyrimspecialedition/mods/97345).

### Q: Why do I have a box in the top right of my screen, or why is my UI not at the edge of my screen?
> A: I only own 16:9 monitors and I don't care to support ultrawide, especially when there aren't patches for all the UI mods that I use.

### Q: How do I swap to the NSFW profile, or vice-versa?
> A: Open Mod Organizer. Somewhere along the top will show what profile you have selected, by default it should be `Twisted Skyrim SFW`. Just swap the drop-down and select the profile you want. It is not recommended to swap to the sfw profile, from the nsfw profile mid save. Swapping from the sfw to nsfw profile should work just fine; however, in both of these instances you are on your own for any issues that may arise. I'd recommend viewing the [safe-save guide](https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/README.md#loading-your-saves-and-saving).

### Q: Install failed cause of google drive saying too many requests (or something similar)
> A: [Try this.](https://www.reddit.com/r/google/comments/nfsgal/google_drive_download_quota_limit_exceeded_bypass/)

### Q: Install failed because "Could not find a part of the path"
> A: Delete the file mentioned in the log. Close and reopen Wabbajack, then rerun the installer with the same paths set. Make sure you have at least 80 gbs on your C drive, and plenty of space on your installation drive. If it keeps failing delete the entire `Temp_BSA_FILES` folder, close and reopen wabbajack, then rerun the installer again. If it continues to fail, restart your PC. 

# Known Issues

### [Insert Male NPC] looks like he has tits / has a really big chest and arms!
Solution(s)
> 1. Change their OBody preset, do not report this as an issue to me, OBody has no way to filter for males and disable the "push up" effect.
