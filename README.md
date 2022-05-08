# Auto-Crafter

## Installation [WIP]
### Dependencies

[Advanced Combat Tracker](http://advancedcombattracker.com/)\
FFXIV Parsing Plugin\
[Triggernometry Plugin](https://github.com/paissaheavyindustries/Triggernometry/releases)

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

## Updating

![image](https://user-images.githubusercontent.com/19721540/167280757-2a751156-91fc-400f-8bd6-87cf0cf5df96.png)
1. Update the `Hikarin's Triggers` repository
2. Delete the old `Auto Crafter` trigger folder in the `Local Triggers`
3. Copy the updated `Auto Crafter` trigger from `Hikarin's Triggers` repository
4. Paste it in the `Local Triggers`
5. Enable the `Auto Crafter` Trigger in the `Local Triggers`

## Setup [WIP]
### Vanilla (with ACT and ACT plugins only)

1. Go to Keybind, System tab, and set Confirm to `NUM0`
2. Place first macro in hotbar with keybind `1`

For multi-part macro

3. Set first macro's last line to `/e Macro #1 finished`
4. Place second macro in hotbar with keybind `2`
5. Set second macro's last line to `/e Macro #2 finished`
6. Place second macro in hotbar with keybind `3`
  
### Dalamud Plugins
-

## Usage
```
ALIASES:
  /echo autocraft, /echo ac, /e autocraft, /e ac
USAGE:
  /e autocraft [subcommand]
>>Subcommands:
    <none>        toggles the autocrafting on and off.
    on            turns on autocrafting.
    off           turns off autocrafting.
    [craft count] set the limit of crafted items.
    set [amount]  set the current crafted count to the specified amount.
    reset         reset the current count and the elapsed time to 0.
```
