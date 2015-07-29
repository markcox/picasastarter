# Introduction #
This FAQ Page was copied from:
> URL: http://sites.google.com/site/picasastartersite/home  (with a few additions)

# FAQ #

**1) Picasa doesn't find my pictures on my external hard disk when I attach it to another computer. What to do?**

Probably the drive letter assigned to the external hard disk is different on both computers.

a) You can change the drive letter using this procedure: http://www.wikihow.com/Change-a-Drive-Letter-in-Windows-XP

b) Another possibility is to look over the RunPicasa.bat file under Other Tools at the http://sites.google.com/site/picasastartersite/home site. It maps the drive it is installed on to a fixed directory using the subst command line tool and may be useful.

Remark: If you change the drive letter, normally if you disconnect and reconnect the external hard disk Windows will reuse the last used letter for this hard disk. It is a good idea to choose another drive letter than A, B, C, D, E and F. This way chances are little that you would need to change the drive letter to an already occupied letter... which would be a problem!  One suggestion would be to use the P (for Photos) drive.


---


**2) Can I reuse my existing Picasa database when I want to move it to another place?**

Yes, you can. Follow these steps to reuse your default database:

a) Select the predefined database that is always present in Picasa Starter, and click the button "Explore..." at the right-hand side of the Picasa Starter dialog. A windows explorer window will open at the place the database is located. Select the folders "Picasa2" and Picasa2Albums" located there and do "right-click"/"copy".

b) If you didn't add a new detabase yet, create a new one in Picasa Starter using "New database" and do "Browse..." to choose the folder where you would like to put it (or create a new folder). If you want to share this database between multiple users/computers, make sure you choose a folder that is accessible for all of them (with read AND write access).

c) Select the database you want to copy the original one to, and click "Explore..." for this database as well. Do "right-click"/"Paste" in this directory to put a copy of the original database there.

When you do "Run Picasa" with the new database selected... you should have reused all information. If there is a problem, erase the 2  folders Picasa2 and Picasa2Albums from the new database folder, and recopy them using the procedure above.



---


**3) Can I start Picasa with a custom database without actually seeing PicasaStarter?**

**New In Version 1.5:** A Create Shortcut button has been added to Picasa Starter to simplify this process. It adds a shortcut to Picasa Starter with the selected database to the desktop and optionally to the Apps directory. An option checkbox is provided to have the shortcut bring up a menu of databases to ease selection.

Yes! After you defined one or more custom Picasa Databases by starting Picasastarter normally, you can:

a) Navigate (using windows explorer or My computer) to the place where you saved PicasaStarter.exe on you computer.

b) Create a shortcut to Picasastarter by rightclicking PicasaStarter.exe and choose "Create shortcut".

c) Do right-click on the shortcut and choose "Properties".

d) On the tab "Shortcut" add the following text at the end of the "Target" field: /autorun "[DatabaseName](DatabaseName.md)", with [DatabaseName](DatabaseName.md) the name you gave to the database you want to run Picasa with automatically. The double quotes around [DatabaseName](DatabaseName.md) are only necessary if you have spaces in the database name.
Eg.: "C:\Programs\PicasaStarter\PicasaStarter.exe" /autorun "Test database 1"

This shortcut can be renamed and placed wherever you want of course... par example on your desktop.


---


**4) Can I create a "portable" solution for Picasa using PicasaStarter?**


Yes! Picasa itself will still need to be installed on all computers you want to use it on, but all data and settings will be portable.

a) Move all your images to an external harddisk. If you want to reuse your Picasa database, you need to move the images in Picasa itself using the Move Folder command.

**NOTES:**
  * _It is suggested that a folder such as \Pictures be created on the external drive. Then all the pictures and folders to be moved would be moved into this folder._

  * _For the external drive to be portable, All pictures and picture folders must be moved to the external drive, since pictures on other drives will not be available on other computers!_

  * _If you want to keep your pictures in the original locations too, you should back up your original pictures and picasa database, so you can restore them after the end of this procedure._

b) Put PicasaStarter on the external harddisk, for instance in a folder called Picasastarter.

c) Start PicasaStarter from this folder and create a new database, with the "base path" located on the external harddisk, for instance in a folder called Picasadata.

d) Optional: if you want to reuse an existing database, check out frequently asked question nb. 2.

e) Start Picasa from Picasastarter with the new database selected, and immediately go to Tools-Folder Manager.  In Folder Manager, ensure that only the external drive pictures folder and folders with pictures there are selected for "Scan Always". All other folders (Including "My Pictures") should be "Remove From Picasa". Fix them if they aren't.

f) Optional: create a shortcut to PicasaStarter somewhere on the external harddisk as explained in frequently asked question nb. 3.

Now you can attach your external harddisk to any computer having Picasa installed and run PicasaStarter to manage your image collection...
Just remember that the external harddisk must have the same drive letter on all computers, see question 1) above.


---


**5) Is there a Network NAS solution for Picasa using PicasaStarter?**


Yes! Picasa itself will still need to be installed on all computers you want to use it on, but all data and settings can be on the network drive.

The first step is to map the network drive or folder to contain the pictures and data to the same drive letter on all networked computers. The network drive can be either a shared drive (or folder) from another user, or it can be a NAS drive.

It is suggested that unless the drive is to be used only for Picasa, it would be better to make a folder on the drive called something like "Picasa Picture P Drive", and only share that folder and map it to a drive letter such as P: (for pictures). This will improve security since the whole drive will not be shared.

After the Pictures drive is mapped to a drive letter, Just do the procedure for putting the pictures on a portable drive as shown in question **4)** above.

A disadvantage of running Picasastarter from a network drive is you will get a UAC message from windows asking you to confirm that you want to run a program from a network drive.  In Picasastarter 1.5.0 and above you can avoid the UAC by putting a copy of Picasastarter on each local PC and setting it up to get it's settings from the P:\Picasastarter directory _(or wherever the network copy of Picasastarter is located)_. This way Picasastarter will be running from the local PC while sharing the settings on the network.

NOTE: any shortcuts on the local PC should be for the local copy of Picasastarter in this case.


---


**Remark:** making a backup of all images + metadata like face tags,... becomes quite easy on portable of network drives as well: just make a copy of the entire drive.


---


**6) Can I make collages and movies in Picasa when using PicasaStarter?**

Yes, with limitations:
PicasaStarter can only work externally to Picasa, so we can re-map directories and drives and trick Picasa into running with another database, but we can't get inside it where collages and movies are made. Because of this, Windows XP can only view movies and collages, not create or edit them, while Windows 7 can create and edit them subject to some limitations.

You can view both collages and movies in XP by doing what I will describe below, but you cannot edit or create them. Windows 7 is a better case, you can create, edit, and view both collages and movies in win7 (Note, I have only tried this in the 64 bit version of win7).

After you have created a collage in Win7, go into Tools-Folder Manager, and browse to your Database directory, then browse in that directory to the "PICASA\COLLAGES" folder and set it to SCAN ALWAYS. (For Example: My database is on the P: drive in the DatabaseP folder so I browsed to P:\databasep\picasa\collages, and set it to scan always) Your collages will show up in the "Collages" folder in your folders list in addition to the "Other Stuff" list. You will be able to use "locate on disk" edit collage, etc. in the folder list location.

The same steps apply to movies you create using the Picasa Movie creation feature, except the folder to Scan Always is the "PICASA \MOVIES" folder. For some reason, a second movies folder is shown in the "Other Stuff" list rather than in the folders list as the collages were.

You may have to exit and restart Picasa for the new collages and movies folders to show up. Once they show up you can view them in XP also.

Warning: trying to edit movies in XP sometimes causes Picasa to lock up or crash. Trying to edit collages just seems to cause them to not be created or changed.