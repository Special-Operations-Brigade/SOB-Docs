# Vehicle Control System

**Author**: Arcanist

- [Vehicle Control System](#vehicle-control-system)
  - [Introduction](#introduction)
  - [Zeus Module](#zeus-module)
  - [3den Module](#3den-module)
  - [Activation](#activation)
  - [Use Cases](#use-cases)

## Introduction

A new system can be implemented to attach vehicles to some form of control panel. This "Control Panel" or "Console" (as they will be referenced henceforth), can be anything place able within zeus or eden, however the intended purpose is for computer styled objects.

This can be implemented both in Zeus or in Eden.

## Zeus Module

A new module is visible in Zeus under the "SOB" category. "Attach Vehicle to Console" can be used to attach a vehicle to some form of console. All you need to do is first drop the module on the vehicle you want to connect, then you'll be prompted to click your designated console. 
If this is the first time the console is being selected, it will default into the "Off" position and turn off the vehicle you attached.
There is no limit to the amount of vehicle you want can attach to a console.

**If you made a mistake and want to start over, simply delete the console, you do not need to delete the vehicles, all of the configuration is attached to the console.**

## 3den Module

The Eden module can be found in the same place as the zeus module however it's used a little differently. The eden module can be placed down anywhere in the world. Edit the module and you will find a "Controllers" and "Vehicles" attribute. Edit each console and vehicle you wish to be connected and give them a unique variable name.
Add the list of variable names of vehicles and controllers you would like to the module, each name separated by a comma (,)

For example `"console1,console2"` or `"turret1,turret2,turret3"`

## Activation

Once you're satisfied with the configuration, to turn it on all you must do it walk over to the console and select "Activate Console". You will see no prompt however I assure you, the vehicles have been turned on. If you wish to turn them off, simple activate the console again.

## Use Cases

- Venator Defence Systems
- De-activating defense systems without needing to destroy them.
- Booby traps (For example, attach 7 AATs to a console, activate the console and oops, you just turned on the enemy motor pool.)
