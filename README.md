# meta-volumio
volumio config for meta

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
