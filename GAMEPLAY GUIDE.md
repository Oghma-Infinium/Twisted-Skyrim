![](https://raw.githubusercontent.com/Oghma-Infinium/Twisted-Skyrim/refs/heads/main/Twisted%20Skyrim%20Logo%20(1).webp)

<p align="center">
  <a href="https://www.nexusmods.com/skyrimspecialedition/mods/87820](https://www.nexusmods.com/skyrimspecialedition/mods/132034">Nexus</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/README.md">Installation</a> |
  <a href="https://loadorderlibrary.com/lists/twisted-skyrim-2">Modlist</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/FAQ.md">FAQ</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/Performance%20Guide.md">Performance Guide</a> |
  Gameplay Guide
</p>

---


<p align="center">
 IN PROGRESS
</p>


# Gameplay guide

## Initial Setup

Before reading this guide, please following the [Installation Guide](https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/README.md) and read through the [FAQ](https://github.com/Oghma-Infinium/Twisted-Skyrim/blob/main/FAQ.md), both of these will answer almost all the questions you will ask.

## Overview

This section will cover the absolute basics of the list. I suggest reading, or at the very least, skimming, all of the linked mod pages in this section if you are unfamiliar with the following mods.

**I suggest looking through the keybinds for the list in game, by pressing F11**

### Core Overhauls

- Twisted Skyrim uses the [_entire_ simonrim suite](https://next.nexusmods.com/profile/SimonMagus/mods?gameId=1704), except for Arena, Blade and Blunt, and Candlehearth. I highly recommend getting familiar with all of his mods. This modlist also has survival mode enabled by default. It makes use of [Survival Mode Improved](https://www.nexusmods.com/skyrimspecialedition/mods/78244), [Starfrost](https://www.nexusmods.com/skyrimspecialedition/mods/97536), and [Journeyman](https://www.nexusmods.com/skyrimspecialedition/mods/92220). To disable survival mode for your playthrough, simply uncheck the checkbox in settings while in game. 

### Combat Foundations

The following mods are considered the "foundations" of the combat and gameplay for Twisted Skyrim:

- [BFCO - Attack Behavior Framework](https://www.nexusmods.com/skyrimspecialedition/mods/117052) introduces attack commitment to the game, for both NPCs and the Player. If you're familiar with MCO, this will be right at home for you.
  - Time your attacks precisely, aggresive NPCs can and will take advantage of poor planning.

- [Stances NG](https://www.nexusmods.com/skyrimspecialedition/mods/117986) adds 3 different stances, which contain unique moveset for each weapon type. 
  - Shift + X to swap stances.

- [TK Dodge RE](https://www.nexusmods.com/skyrimspecialedition/mods/56956) adds dodging to the game
  - Adds I-Frames, which you should take advantage of.
  - Costs stamina, or magika depending on your class, be sure to manage your resources wisely.

- [Combat Pathing Revolution](https://www.nexusmods.com/skyrimspecialedition/mods/86950)
  - It basically completeley overhauls NPC ai in combat. TL;DR it makes them much smarter and is designed specifically for MCO/BFCO. I'd give the mod page a read.

- [Valhalla Combat](https://www.nexusmods.com/skyrimspecialedition/mods/64741?tab=description) Reworks stamina, adds a timed block, stuns, and executions.
  - There is a ton of info in this mod page, be sure to read through it all. 
  - NPCs can't attack when out of stamina, player deals 50% less damage.
  - Attacks cost stamina, missed attacks drain significantly, landed attacks regenerate your stamina.
  - Stamina regenerates slower while blocking; getting hit while out of stamina and blocking can cause you to stagger.

- [Precision - Accurate Melee Collisions](https://www.nexusmods.com/skyrimspecialedition/mods/72347) Adds accurate melee collisions to the game.
  - You can very easily miss attacks if your sword does not directly collide with an enemy, make sure to be precise!
  - Hitstop, if you hit a wall your sword will bounce back and prevent you from attacking for a very brief time.

- [Maxsu Poise](https://github.com/max-su-2019/MaxsuPoise) and [Modern Stagger Lock](https://github.com/max-su-2019/ModernStaggerLock) implement a Poise system Poise Health can be seen on the Special Bar of TrueHUD (the yellow bar above Health on player and target widgets).

- [SCAR](https://www.nexusmods.com/skyrimspecialedition/mods/72014) brings movesets to NPCs, see the mod page for more info.

- [Ultimate NPC Dodging](https://www.nexusmods.com/skyrimspecialedition/mods/120738) brings dodging to NPCs, makes fights less 2 dimensional, and of course more difficult.
 
- [Modern Combat AI](https://www.nexusmods.com/skyrimspecialedition/mods/74716) makes NPCs far more aggresive, meaning you need to space better and carefully plan your attacks.

## Leveling and Progression

Twisted Skyrim modifies the vanilla leveling system to have the player engage with the world around them more. Just using your skills will not be a sufficient enough way to level up, and you'll be more encouraged to explore and complete quests. Below is a general breakdown of what to expect with the leveling and progression system in Twisted Skyrim.

### Changes to leveling

**Leveling speed is still being worked on based on community feedback so this part of the guide will be changed until I find a nice balance.**

<details>
<summary>Experience</summary>
  
Twisted Skyrim uses [Experience](https://www.nexusmods.com/skyrimspecialedition/mods/17751) and [Skyrim Skill Uncapper](https://www.nexusmods.com/skyrimspecialedition/mods/82558) to handle leveling and progression.

- Experience introduces skill caps based on your player level, the formula is found below.
  - `skillCap = 18 + (playerlevel * 2.00)`

- Skyrim Uncapper introduces skill uncapping and a dynamic experience gain based on skill level. There are too many changes I've made to put here but the gist is this:
  - Skills cap at level 255, however, skill forumalas still cap out at 100, this means that skill-based damage will not go beyond what vanilla was intended for.
  - XP gain is also modified and follows a general increasing gain as your level gets higher. Lower levels should take longer to achieve, slowly capping out once you get a skill to level 100, where xp gain returns to normal.
 </details>
 
<details>
<summary>Progression</summary>
  
- Twisted Skyrim still uses a leveled approach to loot and npc scaling. With the all the changes to how NPCs behave, health pools, damage dealt & much more, NPCs shouldn't be sponges like they are in vanilla. They should be a challenging, yet rewarding experience no matter where you are in the game.
  
- Dragons exist in the beginning of the game and you can see them flying around certain areas in the distance, I highly suggest avoiding them until you have better gear than what you start with.

- There are many generic, custom, and vanilla followers in the list and I highly suggest you make use of them, taking on big foes without them will prove very difficult, and even bandit camps will be difficult due to being out-numbered.

- For more information on how loot gets distributed, see [Open World Loot's modpage](https://www.nexusmods.com/skyrimspecialedition/mods/49681)

- Encounter zones have also been overhauled by [Valorbound](https://www.nexusmods.com/skyrimspecialedition/mods/155430). All encounter zones are treated as such: Min level +5 & no max level. What this means is say you walk into Bleak Falls Barrows at level 30, it sets the zone of that dungeon at level 30 and locks it to that. If you enter it at level 1, but the min level is 10. It will be locked at level 15 (10+5). This affects NPC levels, and what variant of an NPC will spawn in any given location. It should create a more challenging experience for the whole playthrough no matter where you are. For more details, see the mod page.

</details>

### Perks
<details>
<Summary>Adamant</Summary>

Twisted Skyrim uses [Adamant](https://www.nexusmods.com/skyrimspecialedition/mods/30191), [Scion](https://www.nexusmods.com/skyrimspecialedition/mods/41639) and [Manbeast](https://www.nexusmods.com/skyrimspecialedition/mods/44746) for its regular, vampire, and werewolf perk systems(respectively) which are overall much more balanced, and each perk actually impacts gameplay significantly. They rework all of the existing trees and I highly recommend reading through it.

</details>

<details>
<Summary>Custom Skills Framework</Summary>

Twisted Skyrim also makes use of the [Custom Skills Framework](https://www.nexusmods.com/skyrimspecialedition/mods/41780) which unlocks the ability to create new perk trees outside of vanilla. In order to access these custom perk trees you will need to use the power in your `powers` menu called `custom skills` which should open a prompt which asks you to pick a tree to open. I recommend starting off by opening your `Destiny` skill tree either through that menu, or the power that is also present called `Destiny`. You will get Destiny skill points after reaching level 1,level 5, level 10, level 15, level 20, level 25 and level 30 for a total of 7 skill points. Each path of the tree goes with whatever build you might be doing, and is limited to 7 points total so power creep doesn't become an issue.

</details>

## Difficulty

**There is still lots of tuning for me to do for this section as well, but currently it is in a decent spot.**

As said previously, I highly recommend having a follower, or multiple. Playing solo in this list is possible, but not recommended and will increase the difficult significantly.

Twisted Skyrim has a unique approach to difficulty, putting an emphasis on resource management, making sure enemies aren't sponges, and intelligent AI. 

To elaborate on AI more, put simply, they are much more aggresive. They use all spells they have in their aresenal unlike vanilla, attack you if you aim a bow at them, and make use of dodging.

A poise system has been added, and if the enemies (or yours) poise gets broken, a stagger will occur which is an opportunity for you, or them to attack without punishment. Archers can take advantage of headshots to deal bonus poise damage to keep them off of you for longer.

Dodging is not locked behind any perks or powers simply because its too important for all types of builds, there is a fairly long delay after a dodge is performed before you can use it again, or move at all to promote intelligent use of it rather than spamming.

[SkyValor](https://www.nexusmods.com/skyrimspecialedition/mods/106240) changes experience gain, damage, health pools, resource regeneration, and much more. Give it a thorough read.

Potions have been signficantly buffed due to the damage and health changes by SkyValor, and I highly recommend staying stocked up.

[Dragon War](https://www.nexusmods.com/skyrimspecialedition/mods/51310) completely overhauls dragon behaviors and resistances. The dragon fights are much more unpredictable and difficult. Reading through this is basically required as without knowing resistances, you're in for a very long fight.

[Skybane - The Logic of Death](https://www.nexusmods.com/skyrimspecialedition/mods/154357) completely overhauls NPC resistances (all of those except dragons). Everything now has a weakness, but is also will have resistances. This means that carrying multiple damage types is highly recommended. 

<Details>
  
<summary>AI</summary>

Using [Modern Combat AI](https://www.nexusmods.com/skyrimspecialedition/mods/74716), [SCAR](https://www.nexusmods.com/skyrimspecialedition/mods/72014), [BFCO - Attack Behavior Framework](https://www.nexusmods.com/skyrimspecialedition/mods/117052), [Combat Pathing Revolution](https://www.nexusmods.com/skyrimspecialedition/mods/86950), & [Ultimate NPC Dodging](https://www.nexusmods.com/skyrimspecialedition/mods/120738), I've made the NPCs infinitely smarter compared to their vanilla counterparts, they will be more aggresive, use potions, and dodge your attacks.

</Details>

Beware the bears.

# Summary
Other than that, it should really just seem like your playing Skyrim after a while. Aside from these changes, I've tried to make the list in a way you can build your character however you want, side with whomever you want and do whatever you want.. Have fun!
