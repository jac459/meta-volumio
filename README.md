# meta-volumio
volumio config for meta

https://www.youtube.com/watch?v=ybQrpgSK1yM&t=34s

Support meta V0.8.15 onwards.

## Setup
### Step 1 : Install in the meta
#### Prerequisite
In order to use this file, you need to have the metadriver installed. Please refere to this page for further instructions:
https://github.com/jac459/metadriver
#### Installation
To install, downnoad the volumio.json file and move it to the "activated" folder.
Check in the file the line with:
```
     "VolumioURI":"http://volumio.local",
```
Most of the Volumio instance have this address but if you changed the default url of your volumio or have multiple volumio instances, please edit the url to put the one corresponding to your own setup.

### Step 2 : Install in the neeo app
In the neeo app, add a device and search for Volumio.
You will find a driver named: Volumio JAC MetaDriver Volumio.
This is the one.
##### Add the device in the room you want.
##### (Mandatory) go to the recipe list and make the volumio recipe visible.
By default, Volumio is an Audio type and not immediately visible.
##### Ensure your using POWER ON and POWER OFF when launching and CLosing the recipe.
Power On and Power Off are the events used by the meta driver in order to listen to the device.
In your case, if you don't do it, you will not be able to see the state change in your volumio software.
##### Choose your shortcuts.
when loading the recipe, you can suppress all the slides except the ones with shortcuts. 

## Usage
### Browsing
Your browsing experience is with My Music list My Playing Queue list and play <=> queue switch.
You will browse music using my music.
when you click on a song or an album, if your switch is on play. It will play immediately. If you put queue, it will be put in your ... queue.
You can see the song in your queue by using the my playing queue list.
### Playing
You play using the play toggle (also attached to the ok button), skip track using next previous and seek throught the progress slider.
You see what you are doing using the status label.
