# Overview

This is a new origin where you begin in one of several variants of a solar system that has many small, habitable moons colonized by your empire before being able to access faster-than-light travel.  Your home system begins disconnected from the hyperlane network but instead has a wormhole.  You won't be contained for long, however, because you start with 30% progress on Wormhole Stabilization.  Instead of guaranteed habitable systems, your home system will contain extra uncolonized, habitable moons and/or planets based on the number of guaranteed neighbors chosen at game start.

New in version 1.1.0 is a variant of the Sol system that starts your empire around the original jovian planet - Jupiter itself!  Suggestion by [Andora](https://steamcommunity.com/profiles/76561198071084874) and [transfemgodtamer](https://steamcommunity.com/profiles/76561199132491978).  Also a special thanks to [doctornull](https://steamcommunity.com/id/doctornull) for finding and helping me stomp out some bugs relating to starting hyperlanes and jovian leagues.

This origin was inspired by comments from [this](https://old.reddit.com/r/Stellaris/comments/nbtz5d/4_habitable_moons/) post on Reddit.

## Notes

Because there isn't a way to remove a technology from an empire, in lieu of starting the game without Hyperspace Travel (Hyperdrive I) technology, I thought it would be a good proxy to start gated behind a wormhole.  Researching the technology early-game will slow initial technological progress, but skipping it will strongly limit expansion options (notably restricting access to space mining and strategic resources).  Beware - it doesn't protect you from jump drives!

# Changes

A brand-new origin "jovian league" with a few custom starting system initializers to choose from, plus events and effects to get things set up and some start-up screens to get you in the mood.

Because I like origins with secondary species, and I had to do the work anyway to support Driven Assimilators and Rogue Servitors, this mod also includes variations for a jovian league for Mechanists, Syncretic Evolution, and Necrophage origins (including Hive Mind Necrophages).  These flavors are only available to pick if the **host** has the appropriate DLC to unlock the respective built-in origin (Utopia for Mechanists and Syncretic Evolution, Necroids for Necrophage).  After the game setup scripts run, your empire is converted to having the relevant built-in origin in order to keep the built-in benefits - most notably Mechanists get higher chances to draw robotics technologies, and Necrophages have their complex conversion process, purge type, buildings, and tradition swaps.

All flavors of the jovian league origin will respect the special features of your empire - generally, ethics, origin, and civics - in the same way as the base game.  Expect to have special buildings such as Temples as a Spiritualist or Chambers of Elevation as non-genocidal Necrophages.

## Localisation

* English by corsairmarks (author)
* German (Deutsch) by [Lucanoria](https://steamcommunity.com/id/Lucanoria)

## Compatibility

If you want to use the additional Mechanists, Syncretic Evolution, or Necrophage variants of the jovian league origin, the game host must own the corresponding DLC (Utopia or Necroids).  In order to support as much of these origins as possible, the variant jovian league origins will convert themselves into their corresponding vanilla origins after the player presses the BEGIN button. This is strictly necessary for Necrophages as it connects to all of the code for necrophage conversion.

The randomization for ideal and "secondary" planet classes for the starting system initializers supports selecting one of the built-in nine habitable planet classes. Mods that alter your planet class and preference after game starts are compatible with this origin, although likely only the homeworld (out of the four initial colonies) will be altered. If you want the classes of the bonus colonies to be different, you can change them via the console with `planet_class = pc_arid` or whatever class you want. Deposits and features can be rerolled for a planet with `effect reroll_deposits = yes` (these are both built-in console commands).

Because the jovian league origin starts the owner with four colonized moons, it has completely custom empire initialization script - that includes setting up deposits, features, and blockers; adding buildings and districts (including those tied the origins or civics), and spawning Pops of the main species (and secondary species if there is one). The empire initialization process from the base game is entirely bypassed - so mods that overwrote that code will not affect jovian leagues for better or worse. The bulk of the code for the jovian league origins runs when empires are initialized before the game starts.

Finally - because this mod does not overwrite _any_ base game files or code, it should play nicely with many other mods.  Built for Stellaris version 3.4 "Cepheus."  This mod is not compatible with achievements.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it is a new origin.  It is otherwise fully compatible.

### When to Install

This mod should be added before starting a new game.  The main effect of new origins and starting systems are only available during empire creation, and the custom code to set up the new systems only executed during empire initialization.  This mod does define some new deposits and related events, and thus is not recommended to be removed during a game.  If you do choose to remove it, it is highly recommended to take a backup of your savegame before attempting to remove the mod.

### Optional Mod Dependencies

[Planetary Modifier Enhancements](https://steamcommunity.com/workshop/filedetails/?id=2496357128) is used to apply the "Part of an Extensive Moon System" to the initial jovian moon system that hosts your homeworld.

### Recommended Companion Mods

[Yet Another Planetary Sky Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=2527918521) to add visible, ringed gas giants to the planetary sky graphics for your starting colony worlds.  Highly recommended to use another UI-expanding mod such as [Bigger Planet View](https://steamcommunity.com/sharedfiles/filedetails/?id=1587178040) or [Planetary Diversity - Planet View](https://steamcommunity.com/sharedfiles/filedetails/?id=1866576239) to see the full-height planet graphics, which makes the variant skies easier to see.

### Known Issues

The variant jovian league origins will convert themselves into their corresponding vanilla origins after the player presses the BEGIN button (or at game start for AI players). This is necessary to support built-in features for Mechanists, Syncretic Evolution, and Necrophages without needing to duplicate or override all of the relevant code.

Some variants of a jovian league may start with a small negative income of one or more resources. Generally, these can be resolved by prioritizing a job that produces the resource with negative income.

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

## Source Code

[Hosted on  GitHub](https://github.com/corsairmarks/origin_jovian_league)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.