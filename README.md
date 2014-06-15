#blender-vfxtoolbox #

Blender-vfxtoolbox was developed during the production of the short film [senseless](https://vimeo.com/76863099). 

![vfx toolbox](http://zblur.de/github/vfxtoolbox/vfxtoolbox_151_ui-objectmode.jpg "vfxtoolbox 1.5.1 UI-Object Mode")

## Table of Contents ##
- [Installation](#installation)
- [Documentation](#documentation)
    - [Scene Building](#scene-building)
    - [Seek & Destroy](#seek--destroy)
    - [Reconstruction](#reconstruction)
    - [Animation from Ascii File](#animation-from-ascii-file-ascii-tables)
- [Authors](#authors)
- [Thanks](#thanks)
- [Todo](#todo)

## Installation ##

1. Go to User Preferences/Addons
1. Click install from File
1. Activate the addon via VFX category

## Documentation ##

#### Freeze Selection ####
Disables the viewport selection of current objects.

#### Unfreeze All ####
Enables viewport selection of all objects in scene.

### Scene Building ###

#### Add Parent ####
Creates a new empty parent for the selection. It also disables the viewport selection of the new children.

#### Clear Parent ####
Releases all children of the parent, apply their transformations and enables viewport selection.

#### Select Childs ####
Finds all children of a parent and makes them selectable.

### Seek & Destroy ###

#### Find Object Sequence ####
Selects all objects in the scene by the given search string (case sensitive).  
- **cube** selects **cube_001**, **cube.002**, **cube003**
- **cube_** selects **cube_001** but not **cube.002** or **cube003**

#### Rename Selection ####
Renames selection as object sequence. The format can be determined by the number of hash signs.
- **name_###** returns **name_001**, **name_002** ...  
- **name_####** returns **name_0001**, **name_0002** ...

#### Select Cameras & Empties ####
Selects all cameras and empties in scene.

#### Select all Empties in Scene ####
Selects all objects from by type camera and empty.

#### Empties in Selection ####
Selects all empties in current selection.

### Reconstruction ###

#### Connect 2 Empties ####
Creates a new polyline (connected vertices) by the positions of the selected empties.

#### Pointcloud from Empties ####
Creates a pointcloud by the positions of the selected empties.

#### Empties from Vertices (Editmode) ####
Creates empties by the position of selected vertices.

#### Empty in Center of Selection (Editmode) ####
Creates an empty in the center position of the selected vertices.

### Empty Appearance ###

#### Update Size ###
Sets the size of selected empties.

#### Plain, Sphere etc. ###
Changes the appearence of the selected empties to choosen type.

### Animation from Ascii File (Ascii tables) ###

#### Build Empty ####
Imports ascii animation data from other packages and creates a new empty with the data.

#### Apply to Selection ####
Applies the data to the selected objects.

#### Supported Object Properties ####
- Location, Rotation, Scale  
- Energy & Color for Lamps
- Focal Length & Focus Distance for Cameras

#### Options ####
- Change columns of Ascii Table   
- Shift timeline starting point  
- Offset animation keys  
- Multiply all values  
- Add values  


## Authors ##

- [Christian Brinkmann](http://www.zblur.de)
- [David Wiesner](https://github.com/DavidWiesner)

## Thanks ##

- David Wiesner
- Sebastian König
- CoDEmanX

## Todo ##

- Export Animations to Ascii


