# Auto-Crafter

## About
An FFXIV Auto Crafter as an ACT Triggernometry trigger, but why?
- not another application you need to open (if you always have ACT open)
- uses log lines to indentify the next step, for reliability and efficiency
- doesn't actually require any of your act plugins to be up to date in order to function!

Basically, this will likely never break, unless there's a change with the act parsing plugin log syntax

## Features

Elapsed time

Multi-part macro support

Synthesis limit

Auto-pause (and BEEPS!!!) for conditions like

- Spiritbonded 12 items to 100%.
- Losing the effect of food or potion buffs.
- Losing the effect of FC or squadron buffs.
- Equipment durability dropping to 0%.
- Reaching the specified synthesis count.
- Running out of materials.
- Failing a synthesis.
- Most in-game chat log errors in red text

Optional support and extra features using 3rd-party Dalamud Plugins such as

  - Keybindless automation
  - Conditional crafting steps
  - Smart action queuing
  - Extended macro length


## Installation
### Dependencies

   - [Advanced Combat Tracker](http://advancedcombattracker.com/)
   - FFXIV Parsing Plugin
   - [Triggernometry Plugin](https://github.com/paissaheavyindustries/Triggernometry/releases)

### Optional Dependencies
Dalamud Plugins:
   - Telesto
   - [SomethingNeedsDoing](https://raw.githubusercontent.com/daemitus/MyDalamudPlugins/master/pluginmaster.json)
   - MacroChain

### Adding the Trigger


![image](https://user-images.githubusercontent.com/19721540/167280273-e2eeb7d4-66d0-4335-80c4-ed8e0e8725d3.png)

Address: 
```
https://raw.githubusercontent.com/gynryiie/Auto-Crafter/master/TriggernometryExport.xml
```

![image](https://user-images.githubusercontent.com/19721540/167268633-243f8e6f-3379-423f-bdd1-4ec42fe6ac09.png)
![image](https://user-images.githubusercontent.com/19721540/167280269-88339a88-856e-4c20-88b8-4a882533ceae.png)
![image](https://user-images.githubusercontent.com/19721540/167280449-d64d2fb2-b477-4057-96db-8bf50eb1e535.png)
![image](https://user-images.githubusercontent.com/19721540/167280607-27b8c9ad-9aa0-4a9a-9d51-fc6e06ec94b2.png)

Make sure not to have more than 1 instance of the `Auto Crafter` folder trigger enabled

## Updating

![image](https://user-images.githubusercontent.com/19721540/167280757-2a751156-91fc-400f-8bd6-87cf0cf5df96.png)
1. Update the `Hikarin's Triggers` repository
2. Delete the old `Auto Crafter` trigger folder in the `Local Triggers`
3. Copy the updated `Auto Crafter` trigger from `Hikarin's Triggers` repository
4. Paste it in the `Local Triggers`
5. Enable the `Auto Crafter` Trigger in the `Local Triggers`

## Setup
### With Vanilla Client (ACT and ACT plugins only)

1. Go to `Keybind`, `System` tab, and set `Confirm` to `NUM0`
2. Place first macro in hotbar with keybind `1`

For multi-part macro

3. Set first macro's last line to `/e Macro #1 finished`
4. Place second macro in hotbar with keybind `2`
5. Set second macro's last line to `/e Macro #2 finished`
6. Place third macro in hotbar with keybind `3`\
   and so on...
### With ACT and Dalamud Plugins
1. Install the required Plugins
2. Download `SomethingNeedDoing.json` from the files above.
3. Cut/Copy and Paste it in `%appdata%\XIVLauncher\pluginConfigs`
4. Enter `/pcraft` in game to open SomethingNeedsDoing
5. Add your macros with a unique title.
6. Add the command `/waitaddon "Synthesis"` at the start of all your macros
7. Set your active macro using the command `/e ac macro snd [macro name]`
## Usage
```
ALIASES:
  /echo autocraft, /echo ac, /e autocraft, /e ac
USAGE:
  /e autocraft [subcommand]
>>Subcommands:
    <none>                  toggles the autocrafting on and off.
    on                      turns on autocrafting.
    off                     turns off autocrafting.
    pause                   pause autocrafting after the current macro is finished.
    [craft count]           set the limit of crafted items.
    set [amount]            set the current crafted count to the specified amount.
    reset                   reset the current count and the elapsed time to 0.
    macro keybind [1-9]     set the initial keybind to be used for crafting.
    
[Requires: Telesto, MacroChain]
    macro shared [0-99]     set the in-game macro from the shared tabs to be used for crafting.
    macro individual [0-99] set the in-game macro from the individual tabs to be used for crafting.
        
[Requires: Telesto, SomethingNeedsDoing]
    macro snd [macro name]  set the SND macro to be used for crafting.
    extract                 extracts all materia from spiritbonded items
```
