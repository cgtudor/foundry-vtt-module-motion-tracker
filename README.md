# foundry-vtt-module-motion-tracker
A module giving life to the Alien RPG motion tracker in foundry VTT

The module installs a button just over the chat box that you can hit.
When hitted, the button will scan for the nearest active and visibles tokens based on the selected token.

## Player visibility control
* In the window I added options to control visibility, just click on the arrow
* Assitants and GMs can control who sees the Motion Tracker, GM has priority over Assistants
* When players hit the Motion Tracker button, Assistants & GMs are notified opening automatically the MTs window
* Opening the MTs does not automatically trigger the visibility for every player as before, so be aware of that
* Greyed players are the one disconnected
* The player with a color is the owner, the one whose tokens have been used with the MT, if there is no one with a color, you are the owner

## Audio
* Audio is supported now, it uses 4 clips of 1 second
* All clips are configurable through the module options

# Changelog

## v1.5.2
* remove dependency from Alien RPG System
* fixed a bug probably coming from Foundry removing once supported 'ife' operation from handlebars

## v1.5.1
* v12 portability

## v1.5.0
* Added screen glitch visual effect
* Added faked signals feature, provides a way to simulate movement points that doesn't exist
Both features might be of use to simulate a glitchy Motion Tracker

## v1.4.1
* Added an option to invert token filtering

## v1.3.1
* Fix init motion tracker broken
* Fix fast token change not working
* Definitely removed the chat button hack

## v1.3.0
* Add feedback when no actor is selected before starting the motion tracker
* Added an option to fast change reference token without closing the app

## v1.2.0
* Fixed last bugs introduced in v1.1.0, thanks to CodaBool
* Added a control menu button to activate motion tracker, we plan to remove the old one later on
* Updated some versions in the localizations

## v1.1.2
* Fixed bugs introduced in v1.1.0
  * Statuses in settings no more taken into account when "scan for players" is turned off
* Fixed warnings, thanks to Txus

## v1.1.1
* Fixed bugs introduced in v1.1.0
  * Statuses in settings no more taken into account
  * Audio settings for volume no longer working

## v1.1.0
* Support of Foundry VTT v11
* Pixi migration to v7
Contribution from CodaBool

## v1.0.0
* Support of Foundry VTT v10
* Disabled audio by default because of v10 sound API issue unloading an audio once it stops

## v0.5.8
* Added french localization (by JNQ)
* Increased max scan speed from 0.01 to 0.1 as per issue https://github.com/pplans/foundry-vtt-module-motion-tracker/issues/43

## v0.5.7
* Fix Exception if token has a broken actor

## v0.5.6
* Fix Motion Tracker not shareable anymore with players
* Fix scan players option

## v0.5.5
* Migration to 8.x foundry series, audio

## v0.5.4
* Migration to 8.x foundry series, first step

## v0.5.3
* Fix ES language not in the module.json

## v0.5.2
* Added ES language by KaWeNGoD

## v0.5.1
* Quickfix : error when new settings aren't set

## v0.5.0
* Hidden token does not count anymore for the Motion Tracker filtering, you now have to use the statuses
* Added a configuration panel for statuses

## v0.4.1
* Fixed post process animation for Arious not following after a while

## v0.4.0
* Added theme system
* Added Arious theme

## v0.3.0
* Added player visibility control
* A lot of bugs have been fixed among them: not so circular scanning, distance computation

## v0.2.0
* Added full audio support

## v0.1.4
* Fixed a crash when you removed an actor and still had tokens in the scene

## v0.1.3
* Fixed statuses not properly taken into account

## v0.1.2
* Added the "see players" setting behavior so that it will work now (sorry I let it there that long without adding the functionality)

## v0.1.1
* Fixed errors when you first activated the Module in your world
* Fixed a few masqued errors

## v0.1
* Migration Three JS -> PIXIjs taking advantage of the engine already in use inside Foundry VTT
* Added animations for both signals and background simulating periodic scan
* Added text giving distance of nearest ping detected
* Improved background texture, adding a frame for text + a red spot for origin
* Fixed a lot of bugs:
  * A taken right over the player is no longer detected
  * Improved resource loading

## v0.0.4
* fixes on player view streaming

## v0.0.3
* statuses affects the motion tracker scanner now
* motion tracker is renderer in a window and is now draggeable => removed settings to center and offset
* improved ping textures
* once the tracker is enabled, the origin remains the same and is streamed correctly

## v0.0.2
* resize

## v0.0.1
If you select another token the display will update.
Moving tokens will update the display also.
Clicking on the button again will hide the motion tracker.
The motion tracker is visible for everyone, there is an option in the settings to only allow having the button for the GM, but it won't update an UI already rendered so you have to kick your players out.

## Roadmap
### Customisation
* Two more themes : the old Motion Tracker with green screen and a Med-Fan one

### Configurable statuses
* Make the statuses that are filtered configurable

### Synchronize settings and player sessions

### Investigate on check or not if we can get the player with the Motion Tracker

# Special thanks
Otakode - some indirect ideas and his feedbacks
Freki - pushing me around to make this happen and giving me a lot of ideas and feedbacks
Sasmira - a lot of feedbacks and contradictory ideas that are valued
Minarkhaios - fadeout
CodaBool - v11 & Pixi v7 migration
KaWeNGoD - for the Spanish localization
JNQ - for the French localization
Truncated - for the module.json update
IcedEagle - v12 migration
Foundry community, specially Alien RPG one
Some parts of the code may resemble to dice-so-nice sources, this project is actually based on dice-so-nice and tends to get as far as possible to it with time
