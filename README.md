# PSYCHRONIC_MegaSaveMZ

**RPG Maker MZ Plugin**

Adds Extra Functionality to the Save/Load Screen for RPG Maker MZ.

## What It Does

This plugin completely overhauls the save/load screen in RPG Maker MZ.

## Plugin File

- `PSYCHRONIC_MegaSaveMZ.js`
- Target: RPG Maker MZ
- Author: Psychronic
- URL: https://psychronic.itch.io

## Plugin Commands

- `triggerAutosave`

## Parameter Summary

- FileListSettings
- maxSaveFiles: Maximum number of manual save files (not counting autosave).
- fileListWidth: Width of the file list column in pixels.
- fileItemHeight: Height of each file slot in pixels.
- autosaveIcon: Icon for autosave slot in the save menu list (0 = no icon). For popup icon, use \i[x] in popup text.
- savedFileIcon: Icon for slots with save data (0 = green square).
- emptyFileIcon: Icon for empty slots (0 = gray square).
- DisplaySettings
- autosaveText: Text to display for the autosave slot.
- gameTitle: Game title shown below the command buttons.
- showMapName: Show the current map name between characters and stats.
- CommandSettings
- loadCommandIcon: Icon index for Load button (0 = no icon).
- saveCommandIcon: Icon index for Save button (0 = no icon).
- deleteCommandIcon: Icon index for Delete button (0 = no icon).
- loadCommandText: Text for Load button. Use \i[x] for inline icons.
- saveCommandText: Text for Save button. Use \i[x] for inline icons.
- deleteCommandText: Text for Delete button. Use \i[x] for inline icons.
- showDeleteCommand: Show the Delete command button.
- AutosaveSettings
- showAutosavePopup: Show a notification popup when autosave completes.
- autosavePopupText: Text to display in the autosave popup. Use \i[x] to manually add icons if desired.
- autosavePopupDuration: How long the popup stays on screen (in frames, 60 = 1 second).
- autosavePopupPosition
- autosavePopupOffsetX: Horizontal offset from the edge (in pixels).
- Additional parameters are documented in the plugin header/help text.

## Installation

1. Download `PSYCHRONIC_MegaSaveMZ.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.
4. Configure any plugin parameters or commands listed below.

## Full Plugin Help

### Introduction

This plugin completely overhauls the save/load screen in RPG Maker MZ.

Features:
- Display character sprites on save files
- Three configurable statistics columns
- Customizable command buttons (Load/Save/Delete)
- Support for text codes like \i[52], \c[3] in stat labels
- Autosave slot as first entry in save list
- Plugin command to trigger autosave
- Customizable autosave popup notification
- Configurable autosave sound effect

### Notes

- The Autosave Icon parameter only affects the save menu list
- To add an icon to the popup, manually include \i[x] in the popup text
- Example: Set popup text to "\i[652] Autosave Complete"

### Plugin Commands

Trigger Autosave
- Saves the current game to the autosave slot (appears first in list)
- Use this in events to create manual autosave points
- Shows popup notification if enabled
- Plays custom sound effect if configured

### Terms of Use

Free for commercial and non-commercial use.
Credit Psychronic in your game.

@param FileListSettings
@text File List Settings

@param maxSaveFiles
@text Max Save Files
@parent FileListSettings
@type number
@min 1
@max 999
@default 50
@desc Maximum number of manual save files (not counting autosave).

@param fileListWidth
@text File List Width
@parent FileListSettings
@type number
@min 100
@max 400
@default 160
@desc Width of the file list column in pixels.

@param fileItemHeight
@text File Item Height
@parent FileListSettings
@type number
@min 20
@max 100
@default 36
@desc Height of each file slot in pixels.

@param autosaveIcon
@text Autosave Icon
@parent FileListSettings
@type number
@min 0
@default 0
@desc Icon for autosave slot in the save menu list (0 = no icon). For popup icon, use \i[x] in popup text.

@param savedFileIcon
@text Saved File Icon
@parent FileListSettings
@type number
@min 0
@default 0
@desc Icon for slots with save data (0 = green square).

@param emptyFileIcon
@text Empty File Icon
@parent FileListSettings
@type number
@min 0
@default 0
@desc Icon for empty slots (0 = gray square).

@param DisplaySettings
@text Display Settings

@param autosaveText
@text Autosave Text
@parent DisplaySettings
@type text
@default Autosave
@desc Text to display for the autosave slot.

@param gameTitle
@text Game Title
@parent DisplaySettings
@type text
@default Star-Shift: Freelancers
@desc Game title shown below the command buttons.

@param showMapName
@text Show Map/Location Line
@parent DisplaySettings
@type boolean
@default true
@desc Show the current map name between characters and stats.

@param CommandSettings
@text Command Button Settings

@param loadCommandIcon
@text Load Icon
@parent CommandSettings
@type number
@default 0
@desc Icon index for Load button (0 = no icon).

@param saveCommandIcon
@text Save Icon
@parent CommandSettings
@type number
@default 0
@desc Icon index for Save button (0 = no icon).

@param deleteCommandIcon
@text Delete Icon
@parent CommandSettings
@type number
@default 0
@desc Icon index for Delete button (0 = no icon).

@param loadCommandText
@text Load Button Text
@parent CommandSettings
@type text
@default LOAD
@desc Text for Load button. Use \i[x] for inline icons.

@param saveCommandText
@text Save Button Text
@parent CommandSettings
@type text
@default SAVE
@desc Text for Save button. Use \i[x] for inline icons.

@param deleteCommandText
@text Delete Button Text
@parent CommandSettings
@type text
@default DELETE
@desc Text for Delete button. Use \i[x] for inline icons.

@param showDeleteCommand
@text Show Delete Button
@parent CommandSettings
@type boolean
@default true
@desc Show the Delete command button.

@param AutosaveSettings
@text Autosave Settings

@param showAutosavePopup
@text Show Autosave Popup
@parent AutosaveSettings
@type boolean
@default true
@desc Show a notification popup when autosave completes.

@param autosavePopupText
@text Autosave Popup Text
@parent AutosaveSettings
@type text
@default Autosave Complete
@desc Text to display in the autosave popup. Use \i[x] to manually add icons if desired.

@param autosavePopupDuration
@text Popup Duration
@parent AutosaveSettings
@type number
@min 30
@max 600
@default 120
@desc How long the popup stays on screen (in frames, 60 = 1 second).

@param autosavePopupPosition
@text Popup Position
@parent AutosaveSettings
@type select
@option Top Left
@value topLeft
@option Top Right
@value topRight
@option Bottom Left
@value bottomLeft
@option Bottom Right
@value bottomRight
@default topRight
@desc Where the autosave popup appears on screen.

@param autosavePopupOffsetX
@text Popup Offset X
@parent AutosaveSettings
@type number
@min -500
@max 500
@default 20
@desc Horizontal offset from the edge (in pixels).

@param autosavePopupOffsetY
@text Popup Offset Y
@parent AutosaveSettings
@type number
@min -500
@max 500
@default 20
@desc Vertical offset from the edge (in pixels).

@param playAutosaveSound
@text Play Autosave Sound
@parent AutosaveSettings
@type boolean
@default true
@desc Play a sound when autosave completes. Turn off for silent autosaves.

@param autosaveSoundName
@text Autosave Sound Name
@parent AutosaveSettings
@type file
@dir audio/se
@desc Sound effect file to play on autosave. Leave blank for default save sound.

@param autosaveSoundVolume
@text Autosave Sound Volume
@parent AutosaveSettings
@type number
@min 0
@max 100
@default 90
@desc Volume of the autosave sound effect (0-100).

@param autosaveSoundPitch
@text Autosave Sound Pitch
@parent AutosaveSettings
@type number
@min 50
@max 150
@default 100
@desc Pitch of the autosave sound effect (50-150).

@param autosaveSoundPan
@text Autosave Sound Pan
@parent AutosaveSettings
@type number
@min -100
@max 100
@default 0
@desc Pan of the autosave sound effect (-100 to 100).

@param InfoColumns
@text Information Columns

@param useVariableNames
@text Use Database Variable Names
@parent InfoColumns
@type boolean
@default true
@desc If true, empty labels will use variable names from database. If false, shows "Variable X".

@param column1Stats
@text Column 1 Stats
@parent InfoColumns
@type struct<StatDisplay>[]
@default ["{\"label\":\"Location\",\"type\":\"mapName\",\"variableId\":\"0\",\"iconIndex\":\"0\"}","{\"label\":\"Playtime\",\"type\":\"playtime\",\"variableId\":\"0\",\"iconIndex\":\"0\"}","{\"label\":\"Total Saves\",\"type\":\"saveCount\",\"variableId\":\"0\",\"iconIndex\":\"0\"}","{\"label\":\"\\\\i[314] Credits\",\"type\":\"gold\",\"variableId\":\"0\",\"iconIndex\":\"0\"}","{\"label\":\"Missions Completed\",\"type\":\"variable\",\"variableId\":\"4\",\"iconIndex\":\"0\"}","{\"label\":\"Loyalty (Crew)\",\"type\":\"variable\",\"variableId\":\"61\",\"iconIndex\":\"0\"}","{\"label\":\"CYBERNET RANK\",\"type\":\"variable\",\"variableId\":\"200\",\"iconIndex\":\"0\"}"]
@desc Statistics to display in column 1.

@param column2Stats
@text Column 2 Stats
@parent InfoColumns
@type struct<StatDisplay>[]
@default ["{\"label\":\"\\\\i[87] Reputation (ESA)\",\"type\":\"variable\",\"variableId\":\"1\",\"iconIndex\":\"0\"}","{\"label\":\"\\\\i[87] Reputation (NVS)\",\"type\":\"variable\",\"variableId\":\"2\",\"iconIndex\":\"0\"}","{\"label\":\"\\\\i[87] Reputation (ORC)\",\"type\":\"variable\",\"variableId\":\"6\",\"iconIndex\":\"0\"}","{\"label\":\"\\\\i[87] Reputation (KRYLL)\",\"type\":\"variable\",\"variableId\":\"35\",\"iconIndex\":\"0\"}","{\"label\":\"\\\\i[87] Reputation (Overall)\",\"type\":\"variable\",\"variableId\":\"8\",\"iconIndex\":\"0\"}","{\"label\":\"Ground Units\",\"type\":\"variable\",\"variableId\":\"69\",\"iconIndex\":\"0\"}","{\"label\":\"Fleet Units\",\"type\":\"variable\",\"variableId\":\"70\",\"iconIndex\":\"0\"}"]
@desc Statistics to display in column 2.

@param column3Stats
@text Column 3 Stats
@parent InfoColumns
@type struct<StatDisplay>[]
@default ["{\"label\":\"Member Worlds\",\"type\":\"variable\",\"variableId\":\"71\",\"iconIndex\":\"0\"}","{\"label\":\"Diplomacy\",\"type\":\"variable\",\"variableId\":\"65\",\"iconIndex\":\"0\"}","{\"label\":\"Empathy\",\"type\":\"variable\",\"variableId\":\"3\",\"iconIndex\":\"0\"}","{\"label\":\"Aggression\",\"type\":\"variable\",\"variableId\":\"66\",\"iconIndex\":\"0\"}","{\"label\":\"Honesty\",\"type\":\"variable\",\"variableId\":\"22\",\"iconIndex\":\"0\"}","{\"label\":\"Intelligence\",\"type\":\"variable\",\"variableId\":\"7\",\"iconIndex\":\"0\"}","{\"label\":\"Greed\",\"type\":\"variable\",\"variableId\":\"72\",\"iconIndex\":\"0\"}"]
@desc Statistics to display in column 3.

## Source

This standalone repository is generated from the latest PSYCHRONIC plugin source in the RPG Reactor Complex template.

## License

MIT. See `LICENSE`.
