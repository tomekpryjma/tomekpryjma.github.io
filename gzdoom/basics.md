# Simplest gzdoom map with custom script
These are the steps I did to get a basic cube of a map as well as printing "hello world" on screen.<br/>
I will use Doom's ACS for this as I currently don't know Zscript.

1. Download GZdoom
2. Download ACC (https://github.com/ZDoom/acc)- compiler for ACS
3. Download SLADE- the map and resource editor
4. Make a new project folder, make sure to unzip Gzdoom in that directory
5. Make a new archive (WAD) in slade & add a map (choose Hexen game as base, as this has the ACS scripting)
6. Make a new entry/lump in the WAD of text type, put some acs in there and compile it
7. Save WAD, launch map