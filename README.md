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

### Column 3 Stats

- Command: `triggerAutosave`
- Description: Statistics to display in column 3.

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
- autosavePopupPosition: Where the autosave popup appears on screen.
- autosavePopupOffsetX: Horizontal offset from the edge (in pixels).
- Additional parameters are documented in the plugin header/help text.

## Installation

1. Download `PSYCHRONIC_MegaSaveMZ.js`.
2. Place it in your RPG Maker MZ project's `js/plugins/` folder.
3. Enable it from the RPG Maker Plugin Manager.
4. Configure any plugin parameters or commands listed below.

## Full Plugin Help

PSYCHRONIC_MegaSaveMZ.js

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

## Source

This standalone repository is generated from the latest PSYCHRONIC plugin source in the RPG Reactor Complex template.

## License

MIT. See `LICENSE`.
