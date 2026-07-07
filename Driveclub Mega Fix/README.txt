Driveclub Mega Fix -- by ctrl

---------------------------
THANKS TO:

Nenkai - 010 Editor template for dc.tour
---------------------------

---------------------------
ABOUT THIS MOD
---------------------------

This mod removes all DLC license checks from Driveclub's files, making all DLC playable content (cars, tours, bikes, and bike tours) available without having the DLC packages installed. If you would like to know how this was done, check the Technical Details section.

This mod also changes the online Club unlock cars to be unlocked through player level progression and not Club level progression. This allows you to unlock and use the cars in normal gameplay without connection to Driveclub's now defunct online services.

This mod also unlocks all previously paid DLC livery editor decals for use with custom paints

Last but not least, this mod also allows you to customize all cars where customization was previously disabled.

---------------------------
INSTALLATION INSTRUCTIONS
---------------------------

Copy the directories from the zip folder to your Driveclub directory (CUSA00003, CUSA00093, CUSA00064, CUSA00066, or CUSA00879). If your game is unpacked, overwrite files (after making backups of the originals). If your game is not unpacked, Driveclub will read the files you copied into the directory before reading any of the .dat files in the folder. Copy/paste, and you're done.

---------------------------
KNOWN BUGS
---------------------------

None. Please let me know if you see one!

---------------------------
FUTURE UPDATES
---------------------------

Tying DLC cars into progression

---------------------------
TECHNICAL DETAILS
---------------------------

Driveclub stores vehicle information in gamedir/newdata/vehicles.csv, livery information in gamedir/liveryeditor/assets/assets.txt and event information in gamedir/data/databases/dc.tour. 

In vehicles.csv, we change the GameVersions column that the game uses to verify which edition of the game you own (PS+, base, bikes) to match the free KTM 1290 Super Duke (Bikes-PS+ Edition). This reduces the license check for all Bikes to the PS+ Edition, the lowest license that can be used to play a limited portion of Driveclub's full content library. To unlock the rest of the DLC cars, we adjust the Status column to read In-Game for every car that previously read DLC. This skips the associated license check for the car by telling Driveclub that the car is not DLC, and is instead a base game car. As an added convenience to those that may be using the PS+ Edition of Driveclub, all cars are now unlocked for that edition of the game and available to use.

To unlock the events, we modify both the license mask and DLC type of the tour events. For all car DLCs (as well as the Suzuki and Mv Agusta Bikes DLCs), we null out the license mask for the tour. With no license mask to check against, the license challenge always returns true. This however, does not work for the Bikes expansion and the EBR tour, both of which verify against the Bikes Expansion license, and not a license mask. To get around this, we change the tour's type in the file from 04 (Bikes Expansion), to 05 (Bikes DLC). Doing this changes the verification needed to access these events to enable the license mask zeroing we do for the car events, unlocking the events and allowing them to be played without the Bikes Expansion installed.

Finally, to unlock the liveries, we remove all references to "entitlements" and "purchase_entitlements" from gamedir/liveryeditor/assets/assets.txt. This causes the game to no longer attempt a challenge to the license ID as it no longer expects a license ID to check.