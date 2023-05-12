# Overview

A brand-new origin where you begin in a solar system that has many small, habitable moons colonized by your empire before being able to access faster-than-light travel.  Your home system begins disconnected from the hyperlane network but instead has a wormhole.  You won't be contained for long, however, because you start with 30% progress on Wormhole Stabilization.  Instead of guaranteed habitable systems, your home system will contain extra uncolonized, habitable moons and/or planets based on the number of guaranteed neighbors chosen at game start.

There are also variations on the original Origin: Jovian League that mirror some of the built-in origins:

* Mechanists (requires the Utopia expansion)
* Syncretic Evolution (requires the Utopia expansion)
* Necrophage (requires the Necroids Species Pack)
* Lost Colony
* Knights of the Toxic God (requires the Toxoids Species Pack)
* Teachers of the Shroud (requires the Overlord expansion)
* Fear of the Dark (requires the First Contact Story Pack)

Also supported are any of the new "Eager Explorer" civics (requires the First Contact Story Pack) which begin _without_ a wormhole or hyperlane connection to the rest of the galaxy. Enjoy an early spaceflight start and chart your expansion without the use of hyperlanes!

## Special Thanks

* [doctornull](url=https://steamcommunity.com/id/doctornull) for finding and helping me stomp out some bugs relating to starting hyperlanes and jovian leagues
* [Andora](https://steamcommunity.com/profiles/76561198071084874) and [transfemgodtamer](https://steamcommunity.com/profiles/76561199132491978) for 
suggesting Sol system variant that starts your empire around the original jovian planet - Jupiter itself!
* [dsecret88](https://steamcommunity.com/id/Dragyn88) for suggesting the Lost Colony variant
* [zephramwolf](https://steamcommunity.com/profiles/76561198028125519) for suggesting the Knights of the Toxic God variant
* [Undisclosed](https://steamcommunity.com/id/theluin) for suggesting the Teachers of the Shroud variant
* Originally was inspired by comments from [this](https://old.reddit.com/r/Stellaris/comments/nbtz5d/4_habitable_moons/) post on Reddit

# Changes

A brand-new Origin: Jovian League with a few custom starting system initializers to choose from, plus events and effects to get things set up and some start-up screens to get you in the mood.

Because I like origins with secondary species, and I had to do the work anyway to support Driven Assimilators and Rogue Servitors, this mod also includes variations for a jovian league for Mechanists, Syncretic Evolution, and Necrophage origins (including Hive Minds).  These flavors are only available to pick if the **host** has the appropriate DLC to unlock the respective built-in origin.  Also supported are additional origins that are conceptually about space travel and   After the game setup scripts run, your empire is converted to having the relevant built-in origin in order to keep the built-in benefits from that origin, such as tradition swaps, tech weights, or mechanics like necrophage.

All flavors of the jovian league origin will respect the special features of your empire - generally, ethics, origin, and civics - in the same way as the base game.  Expect to have special buildings such as Temples as a Spiritualist or Chambers of Elevation as non-genocidal Necrophages.

## Localisation

* English by corsairmarks (author)
* German (Deutsch) by [Lucanoria](https://steamcommunity.com/id/Lucanoria)

## Compatibility

If you want to use the additional variants of the jovian league origin, the game host must own the corresponding DLC.  In order to support as much of these origins as possible, the variant jovian league origins will convert themselves into their corresponding vanilla origins after the player presses the BEGIN button. This is strictly necessary for necrophages as it connects to all of the code for Necrophage conversion.

The randomization for ideal and "secondary" planet classes for the starting system initializers supports selecting one of the built-in nine habitable planet classes or equivalent classes from [Planetary Diversity](https://steamcommunity.com/sharedfiles/filedetails/?id=819148835).

Because the jovian league origin starts the owner with four colonized moons, it has completely custom empire initialization script - that includes setting up deposits, features, and blockers; adding buildings and districts (including those tied the origins or civics), and spawning Pops of the main species (and secondary species if there is one). The empire initialization process from the base game is entirely bypassed - so mods that overwrote that code will not affect jovian leagues for better or worse. The bulk of the code for the jovian league origins runs when empires are initialized before the game starts.

Finally - because this mod overrides only a single base game code object, it should play nicely with many other mods.  Built for Stellaris version 3.8 "Gemini."  This mod is not compatible with achievements.

### When to Install

This mod should be added before starting a new game.  It is not recommended remove this mod during a game.  If you do choose to remove it, it is highly recommended to take a backup of your savegame before attempting to remove the mod.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it is a new origin.  It is otherwise fully compatible.

### Optional Mod Dependencies

[Planetary Modifier Enhancements](https://steamcommunity.com/workshop/filedetails/?id=2496357128) is used to apply the "Part of an Extensive Moon System" to the initial jovian moon system that hosts your homeworld.

### Recommended Companion Mods

[Yet Another Planetary Sky Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=2527918521) to add visible, ringed gas giants to the planetary sky graphics for your starting colony worlds.  Highly recommended to use another UI-expanding mod such as [Bigger Planet View](https://steamcommunity.com/sharedfiles/filedetails/?id=1587178040) or [Planetary Diversity - Planet View](https://steamcommunity.com/sharedfiles/filedetails/?id=1866576239) to see the full-height planet graphics, which makes the variant skies easier to see.

## Known Issues

The variant jovian league origins will convert themselves into their corresponding vanilla origins after the player presses the BEGIN button (or at game start for AI players). This is necessary to support built-in features for the variants without needing to duplicate or override all of the relevant code.

Some variants of a jovian league may start with a small negative income of one or more resources. Generally, these can be resolved by prioritizing a job that produces the resource with negative income.

### Error Logs

Origin: Jovian League (Teachers of the Shroud) begins with a shroud tunnel in their system.  In order for it to be usable without the Shroud Beacon starbase building, it was necessary to update the conditions for when a shroud tunnel bypass counts as a node. The game logs one error message to indicate the overwrite:

```
[06:41:31][game_singleobjectdatabase.h:165]: Object with key: shroud_tunnel already exists, using the one at  file: common/bypass/10_jovian_league_bypass_overrides.txt line: 2
```

## Changelog

* 1.0.0 Initial version
* 1.1.0 Hyperlane connection bug fixes, add a new jovian league starting system
    * Ensure the jovian league starting systems don't create isolated systems or mini-clusters disconnected from the hyperlane network - special thanks to [doctornull](https://steamcommunity.com/id/doctornull)
    * Add a jovian league variant of the Sol starting system - suggested by [Andora](https://steamcommunity.com/profiles/76561198071084874) and [transfemgodtamer](https://steamcommunity.com/profiles/76561199132491978)
    * Add German localisation by [Lucanoria](https://steamcommunity.com/id/Lucanoria)
* 1.2.0 AI gets extra progress on Wormhole Stabilization
* 2.0.0 Update for Stellaris version 3.3 "Libra"
    * Handle additional of Permanent Employment (including correct system setup and base-game restrictions)
    * Sol starting system has Venus decreased in size (as per the base game)
    * Jovian League setup adjusted for unity buildings and changed game mechanics
    * Fix missing Sol neighbor systems
* 3.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Use memory optimization feature for effects and triggers
    * Convert `localisation_synced` into regular `localisation`
    * Convert `random_names` to the new, localised style
    * Idyllic Bloom gains a Gaia Seeder, as added in 3.4
* 3.1.0 Minor trigger and effect enhancements
* 4.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Each Jovian League variant can only spawn once - it was getting a bit _too_ common
    * Integrate underlying game changes (notably random empire names)
    * Update Jovian League Mechanists to show the correct bonuses and to start with specialized robots
    * Update Jovian League game start scripts to add Environmentalists and Relentless Industrialists buildings
    * Add safety checks to avoid creating the "exit" wormhole in a fallen empire or marauder system
    * Add a jovian league variant of Lost Colony - suggested by [dsecret88](https://steamcommunity.com/id/Dragyn88)
* 4.0.1 Fix a bug with the trigger that helps determine the correct type of generator districts for a planet
* 4.0.2 Bugfix patch
    * Fix a bug where empires were getting (many) Terraforming Candidate modifiers on already-colonizable worlds - they are intended to have a chance to spawn when the number of guaranteed colonies is 0 or 1
    * Fix a bug where Prosperous Unification/Colonial Spirit/Exotic Mountains spawned on the wrong Jovian League planet (was spawning on the first "sibling" instead of the capital)
* 4.0.3 Reroll the random seed between calls to a couple randomized effects
* 5.0.0 Compatibility triggers
    * Add a compatibility trigger for other mods to check whether this one is active
    * Consume the compatibility trigger from another mod
    * Remove old compatibility global flag
* 6.0.0 Update for Stellaris version 3.7 "Canis Minor"
    * The basic Origin: Jovian League also grants the technology option for Planetary Unification
    * Origin: Jovian League (Necrophage) starts with primitives on up to two planets in the starting system, equal to the amount of guaranteed neighbors set at game start
    * Tweak initial jovial league district, building, and Pop spawning
    * Remove obsolete static modifiers
    * All initially-colonized jovian league planets now benefit from Prosperous Unification modifiers
    * Support the new "Eager Explorer" civics for early jump drives - your starting system will not have a wormhole, and you will have one less colonized jovian moon
    * Add a jovian league variant of Knights of the Toxic God - the Keep orbits your initial jovian planet - suggested by [zephramwolf](https://steamcommunity.com/profiles/76561198028125519)
    * Add a jovian league variant of Teachers of the Shroud - instead of a wormhole, begin with a Shroud Tunnel to the Shroudwalkers and progress on the Psionic Theory technology - suggested by [Undisclosed](https://steamcommunity.com/id/theluin)
    * Add a jovian league variant of Fear of the Dark - one of the initial jovian moons belongs to the dissenters
* 6.1.0 Implement flags to prevent hyperlanes being connected to Origin: Jovian League starting systems by Gigastructural Engineering 3.27
* 7.0.0 Update for Stellaris version 3.8 "Gemini"
    * Integrate underlying game changes
    * Update Sol system to use the fancy new entities

## Source Code

[Hosted on  GitHub](https://github.com/corsairmarks/origin_jovian_league)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.