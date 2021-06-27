# Overview

This is a new origin where you begin in one of several variants of a solar system that has many small, habitable moons colonized by your empire before being able to access faster-than-light travel.  Your home system begins disconnected from the hyperlane network but instead has a wormhole.  You won't be contained for long, however, because you start with 30% progress on Wormhole Stabilization.  Instead of guaranteed habitable systems, your home system will contain extra uncolonized, habitable moons and/or planets based on the number of guaranteed neighbors chosen at game start.

This origin was inspired by comments from [this](https://old.reddit.com/r/Stellaris/comments/nbtz5d/4_habitable_moons/) post on Reddit.

## Notes

Because there isn't a way to remove a technology from an empire, in lieu of starting the game without Hyperspace Travel (Hyperdrive I) technology, I thought it would be a good proxy to start gated behind a wormhole.  Researching the technology early-game will slow initial technological progress, but skipping it will strongly limit expansion options (notably restricting access to space mining and strategic resources).  Beware - it doesn't protect you from jumpdrives!

# Changes

A brand-new origin "Jovian League" with a few custom starting system initializers to choose from, plus events and effects to get things set up and some start-up screens to get you in the mood.

Because I like origins with secondary species, and I had to do the work anyway to support Driven Assimilators and Rogue Servitors, this mod also includes variations for a Jovian League for Mechanists, Syncretic Evolution, and Necrophage origins.  These flavors are only available to pick if the **host** has the appropriate DLC to unlock the respective built-in origin (Utopia for Mechanists and Syncretic Evolution, Necroids for Necrophage).  After the game setup scripts run, your empire is converted to having the relevant built-in origin in order to keep the built-in benefits - most notably Mechnists get higher chances to draw robotics technologies, and Necrophages have their complex conversion process, purge type, buildings, and tradition swaps.

## Compatibility

This mod requires Stellaris 3.0 or higher in order to function.  If you want to use the additional Mechanists, Syncretic Evolution, or Necrophage variants of the Jovian League origin, you must own the corresponding DLC (Utopia or Necroids).  In order to support as much of these origins as possible, the variant Jovian League origins will convert themselves into their corresponding vanilla origins after the player presses the BEGIN button. This is strictly necessary for necrophages as it connects to all of the code for necrophage conversion.

The randomization for ideal and "secondary" planet classes for the starting system initializers does not support any new habitable planets classes.  The code will function alongside new planet classes as long as one of the nine default planet classes is selected, otherwise the guaranteed habitable worlds will be Tomb Worlds. If you want the classes to be different, you can change them via the console with `planet_class = pc_arid` or whatever class you want. Deposits and features can be rerolled for a planet with `effect reroll_deposits = yes` (these are both built-in console commands).

Because the Jovian League origin starts the owner with four colonized moons, it has completely custom empire initialization script - that includes setting up deposits, features, and blockers; adding buildings and districts (including those tied the origins or civics), and spawning Pops of the main species (and secondary species if there is onne). The empire initialization process from the base game is entirely bypassed - so mods that overwrote that code will not affect Jovian Leagues for better or worse. The bulk of the code for the Jovian League origins runs when empires are intialized before the game starts.

This mod is not compatible with achievements.

## Known Issues

The variant Jovian League origins will convert themselves into their corresponding vanilla origins after the player presses the BEGIN button (ar at game start for AI players). This is necessary to support built-in features for Mechanists, Syncretic Evolution, and Necrophages without needing to duplicate or override all of the relevant code.

Some highly specific variants of a Jovian League may start with a small negative income of one or more resources. So far, that seems limited to Spiritualist empires when combined with a secondary species and a special-building-providing civic.

## Changelong

* 1.0.0 Initial version

## Source Code

[Hosted on  GitHub](https://github.com/corsairmarks/origin_jovian_league)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.