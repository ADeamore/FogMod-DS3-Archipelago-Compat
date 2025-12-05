
# Dark Souls III Archipelago Fogmod

All credits for the original fogmod code goes to TheFifthMatt:
Original project source: 


[TheFifthMatt-Fogmod](https://github.com/thefifthmatt/FogMod)

## Edits From the original file:
All references to key items have been removed from the pathfinding checks. Ultimately that leaves 12 locations that the fogmod pathfinder cannot locate due to not having key items to get into them. Several cell doors, Firelink *with* the Firecoil Sword, and The First Kiln to name a few. These locations are now entirely ignored by the randomizer in pathfinding. This results in some more odd situations where spawning in the graveyard will almost always be a dead-end. The solution is to fast travel to firelink shrine using the first bonfire as way to avoid softlock. Pathfinding still will allow every non-key-item based location being accessible, and key items *should* function as they do in vanilla. This mod DOES NOT link into archipelago, but is instead made to work alongside it without interfacing directly. 
## Installation Instructions Alongside Archipelago
 1. Grab the most recent build (.zip) [from the releases tab](https://github.com/ADeamore/FogMod-Archipelago-Compat/releases/tag/latest).
 2. Grab the [ds3 archipelago mod](https://github.com/nex3/Dark-Souls-III-Archipelago-client/releases/tag/v3.0.13)
 3. Extract the DS3 Archipelago folder into *any* location, on the same drive as your DS3 installation. It will locate your game from there on its own.
 4. Create a folder inside of the DS3 Archipelago folder named "Fog"
 5. Drag the contents of the fogmod.zip into the folder you just created.
 6. Open config_darksouls3.toml with a text editor
 7. Change the section labeled "mods" to read:
 ```
         mods = [
	        { enabled = true, name = "fog", path = "fog"},
            { enabled = true, name = "randomizer", path = "randomizer" }
        ]
```
 8. next ensure the server you're going to connect to is running.
 9. open the "Randomizer" folder and run `DS3Randomizer.exe`, and thru that application connect to your archipelago server and click "load".
 10. Next open the Fog folder, and run FogMod.exe
 11. Press the "select other mod to merge" button, and locate the `Data0.bdt` file inside of the `Archipelago/Randomizer` folder.
 12. Select the settings you want. (i recommend pacifist mode, as well as all entrances randomized.)
 13. Press "Randomize!"
 14. And finally run `launchmod_darksouls3.bat` to connect to the Archipelago server and begin playing.
## FAQ

#### The first fog door leads me into a dead end, what do i do?

return to the nearest bonfire, and fast travel to firelink shrine.

#### How long does a run usually take?

Idk man, i just work here.

#### Is it possible to softlock?
I don't think so, but randomizers are tricky. I'd be unsurprised if a softlock happened. Use at your own risk. Right now this is *entirely* untested. Glitches and speedrun strats may be required to navigate around fog gates.