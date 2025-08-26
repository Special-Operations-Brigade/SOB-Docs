# Function Reference

## fnc_assemble_canPickupWeapon.sqf

No documentation available.

## fnc_canUnloadMagazine.sqf

No documentation available.

## mti_drones_fnc_canUnpack

**Description:** Checks whether given unit has drones that can be unpacked.  

**Arguments:**
- `_unit` - The unit to check

**Return Value:** canUnpack?  

**Example:**
```

(begin example)
[player] call mti_drones_fnc_canUnpack;
(end)

```

**Author:** Mokka 

## mti_drones_fnc_getDroneAssembleActions

**Description:** Returns child actions for drone assembly based on current inventory.  

**Arguments:**
- `_player` - Player unit

**Return Value:** droneAssembleActions  

**Example:**
```

(begin example)
[ace_player] call mti_drones_fnc_getDroneAssembleActions;
(end)

```

**Author:** Mokka 

## fnc_getUnloadActions.sqf

No documentation available.

## fnc_handlePlayerVehicleChanged.sqf

No documentation available.

## mti_mortar_turret_fnc_initVehicle

**Description:** Inits the mortar turret, creates crew, adds disassembly action  

**Arguments:**
- `_object` - CSW deployed object

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_mortar_turret_fnc_initVehicle;
(end)

```

**Author:** Mokka 

## fnc_onDroneGrenade.sqf

No documentation available.

## mti_drones_fnc_pack

**Description:** Packs up a drone back into the inventory.  

**Arguments:**
- `_unit` - The unit that is packing the drone back up
- `_drone` - The drone being packed up

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_drones_fnc_pack;
(end)

```

**Author:** Mokka 

## fnc_turretChanged.sqf

No documentation available.

## mti_drones_fnc_unpack

**Description:** Unpacks a drone.  

**Arguments:**
- `_unit` - The unit unpacking the drone
- `_packedDrone` - The class name of the packed drone being unpacked

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_drones_fnc_unpack;
(end)

```

**Author:** Mokka 

