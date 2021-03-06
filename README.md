# proc-blender
This is a template/framework for Blender addons with procedural and genetic mesh generation.
It is derived from the [Procedural Mushrooms](https://github.com/leafar-tb/proc-shrooms) addon and refactored for better reusability.
You only need to define the parameters you need using Blender properties and a function generating a mesh from these parameters.
Operators for generating and modifying objects are derived automatically.
(Though you will likely want to replace the default generator.)
See \_\_init\_\_.py and example.py for more info.
You may also refer to the procedural mushrooms repo, though it is structured differently at the moment.

**The following part can be used as basis for the readme of forked repos.**

# Procedural XY
This Blender plugin adds operators for creating procedural XY meshes.
The operators are explained in more detail below.
To install the addon simply point Blender to a [zip](https://github.com/YOUR-USERNAME/YOUR-REPO/archive/master.zip) of this repo.

## Installation and Usage
If you are familiar with Blender, you can probably skip this.

To install the addon, open the User Preferences via *File->User Preferences* (*Ctrl+Alt+u* should work, too).
There go to the *Add-ons* tab and on the bottom click *Install from File*.
Now simply point Blender to the [zip](https://github.com/YOUR-USERNAME/YOUR-REPO/archive/master.zip).
Finally, you have to activate the addon (still in the *Add-ons* tab).
Just find it in the *User* category or using the search bar on the top-left and activate the check box.

To call an operator, hit space in the 3D view and start typing its name, then select it from the the shown suggestions.
(Operator names are highlighted in *italics* in the following sections.)
The operator panel will probably appear towards the left.
There you'll find the settings affecting the operator.
When the name of a setting is not helpful, try hovering the mouse over a value for a longer explanation.
Your changes to the settings are directly applied, so you can also play around with them to see what they do.
(It will use a fresh random seed with each change, so generated results will vary.)

## Generation
Simply call the *Random XY* operator to generate some objects from random parameters.

## Mutation
When invoking the *Mutate XY* operator on a selected object a number of variations is produced based on it.
The amount of change is controlled by a 'radiation' parameter.

## Procreation
The *Combine XY* operator allows you to merge the features of two or more selected objects.
The features of the created objects are either inherited from one parent directly or averaged over the gene pool.

## Fine Tuning
With the *Edit XY* operator you create a copy of an object and get to modify all of the parameters used in its generation.
