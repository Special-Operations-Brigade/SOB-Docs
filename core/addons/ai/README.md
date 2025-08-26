mti_ai
===================

Several AI-related systems and functions.

# Populate AO

## Introduction

"Populate AO" is a module available in 3den and in Zeus that can be used to rapidly populate areas with air/vehicle/infantry patrols as well as infantry garrisons. Because it creates units in real-time - even in the 3den editor - it is a very powerful tool for mission makers to quickly create "cannon fodder" so that they can spend more time building highly-detailed objectives and hand-placing units in strategically important areas.

## Usage

Look for the "Populate AO" module in your right sidebar in either Zeus or 3den. Place it down at the center of your objective and set the parameters according to your needs. Press OK and the script will spawn the units for you.

The "Objective Name" setting is optional and creates group names based on the obj name provided; if you want to be able to easily access the spawned groups eg. in a script later on.

## Adding Your Own Faction

Custom factions can be added by creating a new class in the config parent `MTI_PopulateAO_Factions`. Populate AO **heavily** depends on CfgGroups, so you may need to create a few additional entries there before your faction is ready to be used with this system.

```cpp
class MTI_PopulateAO_Factions {
    class Default {
        scope = 0; // controls visibility of your faction in the Populate AO dialog
        displayName = ""; // this name is used to list your faction in the Populate AO dialog
        side = -1; // which side units spawned from this faction should be created on (can be different from the side they originally were)
        requiredAddons[] = {}; // a list of required external addons (like in CfgPatches) to automatically hide factions with missing dependencies

        groupPath[] = {}; // this should be a three-item array to point to the location of CfgGroups entries for this faction
//        groupPath[] = {"a", "b", "c"}; // where: configFile >> "CfgGroups" >> "a" >> "b" >> "c"

        Inf_Groups[] = {}; // class-names of groups to spawn as normal infantry (eg. Fire Teams, Assault Squads, etc)
        Inf_AA_Groups[] = {}; // class-names of groups to spawn as AA infantry
        Inf_AT_Groups[] = {}; // class-names of groups to spawn as AT infantry
        Sniper_Groups[] = {}; // class-names of groups to spawn as Sniper teams

        Veh_Light_List[] = {}; // class-names of vehicles (in CfgVehicles) to spawn as light vehicles
        Veh_Heavy_List[] = {}; // class-names of vehicles (in CfgVehicles) to spawn as heavy vehicles

        Air_List[] = {};  // class-names of air vehicle (in CfgVehicles) to spawn as air patrols
    };
};
```

### `groupPath[]`

`groupPath[]` forms the heart of the infantry spawning. It is an array that contains exactly three items, which point to the path of your faction's group classes within CfgGroups. An example:

```cpp
class CfgGroups {
    class East {
        class OPF_F {
            class Infantry {
                class OIA_InfSquad {
                    //...
                };
                class OIA_InfSquad_Weapons {
                    //...
                };
            };
        };
    };
};
```

In this case, `groupPath[]` would be

```cpp
groupPath[] = {"East", "OPF_F", "Infantry"}; // since: configFile >> "CfgGroups" >> "East" >> "OPF_F" >> "Infantry"
```

And `Inf_Groups[]` might be

```cpp
Inf_Groups[] = {"OIA_InfSquad", "OIA_InfSquad_Weapons"};
```

