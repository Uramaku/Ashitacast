# Ashitacast
Cast 2017
Ashitacast is a plugin designed to manage your gear swaps.
This is done through an XML file, which should be placed in Ashita/Config/Ashitacast/
and named CharacterName_JOB.xml.  XMLs will be automatically loaded or unloaded whenever you change jobs,
or can be triggered through commands.  There are some included sample files and a list of valid variables.
Equipment is layered precast<action<midcast in one outgoing packet, which ensures that your precast will always lower
your casttime(or ranged time for rng) and your midcast will always be on in time(even on instant casts or rapid shot).

Commands - can use /ashitacast or /ac

/ac load - Attempt to load Charname_JOB.xml.
/ac load Filename.xml - Attempt to load Filename.xml
/ac reload - Reload the active swap XML.
/ac unload - Unload the active swap XML.

/ac naked - Remove all gear.
/ac set SetName [Duration] - Lock SetName on for Duration in seconds(5 if unspecified).
/ac enable [Slot] - Enables gear swaps for the specified slot, or all slots if unspecified.
/ac disable [Slot] - Disables gear swaps for the specified slot, or all slots if unspecified.

/ac action [Target Index] [ma/ws/ja/ra] [action ID if not ra] - Directly sends an action packet through with appropriate swaps.
/ac debug [Optional: On/Off] - Enables or disables debug prints of all equip swaps.  Will toggle if on/off isn't specified.

/ac validate - Print an output of what items in your XML are not currently in your inventory/wardrobes.
/ac gear - Use dressme or packer plugins(packer is prioritized) to automatically collect gear from your currently loaded xml.  Will not work with neither loaded.

/ac help - Display help on commands.
/ac help print - Display help on print commands.
/ac help var - Display help on var commands.

/ac var clear - Clear all user-defined variables.
/ac var set [name] [value] - Set a variable to a specific value.
/ac var inc [Name] [Optional: Amount] - Increase a variable.  Defaults to 1.
/ac var dec [Name] [Optional: Amount] - Decrease a variable.  Defaults to 1.

/ac print augs \"Item Name\" - Prints a code used to reference the augments on an item.
/ac print uvars - Print current values of all user-defined variables.
/ac print vars - Print current values of all built-in variables.
/ac print set [setname] - Print a set.

/ac addset Name - Add your currently equipped gear to your loaded XML under the specified set name.
/ac newxml Name - Create a blank XML and load it(doesn't include rules, just gives you a blank template to add sets to).
