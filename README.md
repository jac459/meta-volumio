# meta-volumio
Volumio config for meta

Driver initiated by JAC459 and vastly enhanced by MHerwege.

https://www.youtube.com/watch?v=ybQrpgSK1yM&t=34s
https://www.youtube.com/watch?v=loi-8xsP1_8

Support meta V1.0.1 onwards.

## Setup
### Step 1 : Install in the meta
#### Prerequisite
In order to use this file, you need to have the meta installed. Please refere to this page for further instructions:
https://github.com/jac459/meta
#### Installation
To install, downnoad the volumio.json file and move it to the "active" folder.

### Step 2 : Install in the neeo app
In the neeo app, add a device and search for Volumio.
You will find a driver named: Volumio.
This is the one.
##### Add the device in the room you want.
##### (Mandatory) go to the recipe list and make the volumio recipe visible.
By default, Volumio is an Audio type and not immediately visible.
##### Ensure your using POWER ON and POWER OFF when launching and Closing the recipe.
Power On and Power Off are the events used by the meta driver in order to listen to the device.
In your case, if you don't do it, you will not be able to see the state change in your volumio software.
##### Choose your shortcuts.
when loading the recipe, you can suppress all the slides except the ones with shortcuts. 

## Usage
### Browsing
Your browsing experience is with the My Music list and My Playing Queue list.

You browse music using My Music.
Each folder contains a menu and a list of subfolders or songs.

The folder menu has options for:
- Playing the content of the folder
- Adding the songs in the folder to the the current queue
- Adding/removing a shortcut to the folder

Selecting a folder will show the content of the folder.
Selecting a song will open a menu with the same options as in the folder menu, but for the specific song.

The playlist folder lists all playlists available.
Beyond the standard menu options, there is also an option in the menu to delete the playlist.

In many places when browsing through the collection, a search function is provided, allowing you to do a character search in the list.

### Queue Management
You can see the songs in your queue by using the my playing queue list.
If music is playing, the currently playing song will be marked.

The queue menu will allow:
- Clearing the queue
- Turn play shuffle and repeat on or off
- Save the current content of the queue to a new or existing playlist

When selecting a song from the queue, you have the possibility to start playing from this song, or to remove the song from the queue.
### Playing
You play using the play toggle (also attached to the ok button), skip track using next or previous and seek throught the progress slider.
You see what you are doing using the status label.
### Radio
Radio stations listed in the My Music list are taken from the favorite radio stations in the Volumio software.
To have radio stations available, you need to create favorites to radion stations in Volumio first.

### Playlists
Volumio has playlist functionality.
Playlists are saved on the Volumio server and will be available from all Volumio UI's.
It is possible to save the current queue to a new or existing playlist.
### Shortcuts
You can create entries in the top level directory beyond the standard provided entries.
Go to the place in the directory you want, and use the add shortcut from the folder menu.
Shortcuts will be added to the top of the My Music list.
In the same way, you can remove a shortcut.
A Clear Shortcuts button removes all shortcuts from the My Music list.

## Note on people willing to control Chromecast through Volumio
### If your volumio host the music source
#### Get access to your volumio ssh
#### Create a Samba share in your volumio
==> Then you need to create a webserver to serve your files to the chromecast as chromecast doesn't read samba
### Mount localy your Samba:
```
sudo mkdir /mnt/volumioShare    (create a fake folder))
sudo mount -t cifs //192.168.1.44/Volumio2Share /mnt/volumioShare (link the samba to the folder
```
### Install a webserver
``` npm install --global http-server```
### Run the server
http-server /mnt/volumioShare
or pm2 start "http-server /mnt/volumioShare"

