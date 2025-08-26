# Development Information
## Introduction

Below, you can find information and examples on how to define new presets and compositions, how to turn objects into containers and some other tricks.

## Custom Presets
Presets are defined in the class `mti_fortify_presets`. Presets can be defined either in the missionConfigFile or the configFile proper (via Addons). Custom presets should always inherit from `class Default;` in order to ensure forwards compatibility (if new features get added).

### Code Example
```cpp
class mti_fortify_presets {
    class Default {
        scope = 0; // controls visibility of the preset, scope > 0 makes it visible
        displayName = ""; // The name of the preset, displayed in the fortify interaction menu
        backpackOnly = 0; // if this is 1, this preset can only be used with backpacks
        category = ""; // Presets can be assigned to a category which will make the ace menu less cluttered
        condition = "true"; // Condition that has to be met in order to further filter who can access a given preset, passed arguments are [_target,_player]
        class Objects {}; // this sub-class contains all objects (from CfgVehicles) that are available in this preset
    };

    class My_Preset: Default {
        scope = 1;
        displayName = "My Cool Preset";
        category = "Misc";
        class Objects {
            class _xx_Land_BagFenceShort {
                name = "Land_BagFenceShort"; // classname in CfgVehicles
                cost = 10; // cost per object, <= 0 for no cost
                limit = 0; // object limit per container, <= 0 for no limit
            };
        };
    };
};
```

## Custom Compositions
Compositions are defined in the class `mti_fortify_compositions`. Compositions can be defined either in the missionConfigFile or the configFile proper (via Addons). Custom compositions should always inherit from `class Default;` in order to ensure forwards compatibility.

In addition to the config entry, the objects that form the composition need to be defined in an extra file. This extra file contains the output of the function `mti_fortify_fnc_objectsGrabber` which grabs nearby objects and compiles them into the composition format.

### The objectsGrabber
The objectsGrabber compiles nearby objects into a format that can later be placed down again as a composition. It is called as follows:

```
[_center, _radius, _compositionName] call mti_fortify_fnc_objectsGrabber
```

* `_center` is the center position around which objects are collected
* `_radius` is the radius in metres out to which objects are considered
* `_outputName` is an optional parameter that can be used to add an identifying name to the output

After the function is successfully run, the output is copied to your clipboard and should be saved to a file **as-is**. This file is then used for the actual composition (see below how to reference it).

### Code Example

```cpp
class mti_fortify_compositions {
    class Default {
        scope = 0; // controls visibility of the composition, scope > 0 makes it visible
        displayName = ""; // the name of the composition, displayed in the fortify interaction menu
        file = ""; // points to the file that contains the actual composition data (in objectsGrabber format)
        cost = 0; // total cost of the composition, subtracted from the container's max composition budget
        createMarker = 0; // Controls whether a marker should be created upon deploy
        markerType = "hd_flag"; // type of marker (from CfgMarkers) to use for this composition [see: https://community.bistudio.com/wiki/Arma_3:_CfgMarkers]
        markerColor = "ColorBlack"; // colour of marker (from CfgMarkerColors) to use for this composition [see: https://community.bistudio.com/wiki/Arma_3:_CfgMarkerColors]
    };

    class My_Composition: Default {
        scope = 1;
        displayName = "My Cool Composition";
        file = "my_composition.sqf"; // output provided by mti_fortify_fnc_objectsGrabber
        cost = 100;
        createMarker = 1;
        markerType = "b_hq";
        markerColor = "ColorOrange";
    };
};
```

## Custom Containers
### Adding Presets to Containers
Any object can be turned into a container by simply "adding" a fortify preset to it. This can be done through the config, or by using `setVariable`.

In either case, a preset **always** needs to be associated with a budget. Setting a preset's budget to -1, will mean it's **infinite**:

```cpp
class CfgVehicles {
    class My_Container {
        //...
        mti_fortify_availablePresets[] = { "My_Preset", 1000, "My_Preset_2", -1 }; // presets in format: <class name>, <total budget>
    };
};
```

The same can be done using the `setVariable` scripting command:

```cpp
My_Container setVariable ["mti_fortify_availablePresets", ["My_Preset", 1000, "My_Preset_2", -1], true];
```

### Adding Compositions to Containers
Any object can be turned into a composition container by simply "adding" a composition to it. This can be done through the config, or by using `setVariable`.

The container uses one single budget for all compositions. If that budget is set to -1, it will be **infinite**.

```cpp
class CfgVehicles {
    class My_Composition_Container {
        //...
        mti_fortify_availableCompositions[] = { "My_Composition" };
        mti_fortify_compositionBudget = 2500;
    };
};
```

The same can be done using the `setVariable` scripting command:

```cpp
My_Composition_Container setVariable ["mti_fortify_availableCompositions", ["My_Composition"], true];
My_Composition_Container setVariable ["mti_fortify_compositionBudget", 2500, true];
```

### Making Save/Load Containers
Any object can be turned into a save/load container by setting some few config parameter (or by setting some variables using `setVariable`).

```cpp
class CfgVehicles {
    class My_Save_Container {
        //...
        mti_fortify_canSave = 1; // enables saving nearby deployed objects into a composition, required
        mti_fortify_saveMaxBudget = 2500; // controls how many objects (based on cost) the container can save, optional
        mti_fortify_saveRange = 100; // controls how far out objects can be in order for them to get saved, optional
    };
};
```

The same using `setVariable`:

```cpp
My_Save_Container setVariable ["mti_fortify_canSave", true, true];
My_Save_Container setVariable ["mti_fortify_saveMaxBudget", 2500, true];
My_Save_Container setVariable ["mti_fortify_saveRange", 100, true];
```

## Custom Fortify Backpacks
As already indicated, access to the Fortify is unlocked by having a special type of backpack equipped. Any backpack can be turned into a Fortify backpack by adding the following parameters to its config:

```cpp
class CfgVehicles {
    class My_Fortify_Backpack {
        //...
        mti_fortify_canFortify = 1; // enables player to access the fortify menu

        // optional, if you want players to be able to deploy things directly from backpack without container:
        mti_fortify_availablePresets[] = { "My_Backpack_Preset", 250 }; // presets in format: <class name>, <total budget>
    };
};
```

## Preset Categories

Preset categories were introduced to reduce the clutter in the Fortify root menu when a lot of containers are nearby. Categories are hard-coded as sub-classes in the self-action tree of `CAManBase`. The `category =` parameter of a preset entry must match the classname of the category *exactly*.

Custom categories can be added following the example below:

```cpp
class CfgVehicles {
    class Man;
    class CAManBase: Man {
        class ACE_SelfActions {
            class MTI_Fortify {
                class My_Category {
                    displayName = "My Own Category";
                    condition = "true";
                    statement = "";
                    showDisabled = 0;
                    insertChildren = "[_this select 0,'My_Category'] call mti_fortify_fnc_addActions"; // IMPORTANT: also replace My_Category with your own classname here!
                };
            };
        };
    };
};
```

## Tricks
### Preset Objects Macro

This handy macro makes defining preset objects a breeze:
```cpp
#define MACRO_FORTIFY_ADD(CLASSNAME,COST,LIMIT) class _xx_##CLASSNAME { \
    name = #CLASSNAME; \
    cost = COST; \
    limit = LIMIT; \
}
```

### Enabling Fortify without backpack
Using `setVariable`, a player can be given access to the Fortify system without having a compatible backpack equipped:

```cpp
player setVariable ["mti_fortify_canFortify", true];
```
