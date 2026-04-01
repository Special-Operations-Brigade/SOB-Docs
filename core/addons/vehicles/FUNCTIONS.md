# Function Reference

## mti_vehicles_fnc_canDeploy

**Description:** Checks whether given vehicle can be deployed (to make fortify available).  

**Arguments:**
- `_vehicle` - The vehicle to check

**Return Value:** canDeploy?  

**Example:**
```

(begin example)
[] call mti_vehicles_fnc_canDeploy;
(end)

```

**Author:** Mokka 

## mti_vehicles_fnc_canPackUp

**Description:** Checks whether given vehicle is deployed and can be packed up.  

**Arguments:**
- `_vehicle` - Vehicle to check

**Return Value:** canPackUp?  

**Example:**
```

(begin example)
[] call mti_vehicles_fnc_canPackUp;
(end)

```

**Author:** Mokka 

## mti_vehicles_fnc_canSwapVehicle

**Description:** Checks whether given vehicle can be swapped by the player. Requires the player to be an engineer and the vehicle to have a swap target defined.  

**Arguments:**
- `_vehicle` - The vehicle to check
- `_player` - The player attempting the swap

**Return Value:** canSwap?  

**Example:**
```

(begin example)
[cursorTarget, player] call mti_vehicles_fnc_canSwapVehicle;
(end)

```

**Author:** Ramsey 

## mti_vehicles_fnc_debug_track

**Description:** Debugging function that tracks fired projectiles. Used to debug Artillery.  

**Arguments:**
- `_vehicle` - Vehicle the projectile was fired from
- `_projectile` - The projectile itself

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_vehicles_fnc_debug_track;
(end)

```

**Author:** Mokka 

## mti_vehicles_fnc_deploy

**Description:** Deploys given vehicle, disables the engine and makes fortify presets available.  

**Arguments:**
- `_vehicle` - Vehicle to deploy

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_vehicles_fnc_deploy;
(end)

```

**Author:** Mokka 

## mti_vehicles_fnc_deployLocal

**Description:** Local deploy handler. Keeps the vehicle's engine from being turned on while vic is deployed.  

**Arguments:**
- `_vehicle` - Vehicle to deploy

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_vehicles_fnc_deployLocal;
(end)

```

**Author:** Mokka 

## mti_vehicles_fnc_getSwapVehicleActions

**Description:** Returns child actions for each available vehicle swap option.  

**Arguments:**
- `_target` - The vehicle to swap
- `_player` - The player performing the interaction

**Return Value:** Array of actions  

**Example:**
```

(begin example)
[cursorTarget, player] call mti_vehicles_fnc_getSwapVehicleActions;
(end)

```

**Author:** Ramsey 

## mti_vehicles_fnc_packUp

**Description:** Packs up given deployed vehicle.  

**Arguments:**
- `_vehicle` - Vehicle to pack up

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_vehicles_fnc_packUp;
(end)

```

**Author:** Mokka 

## mti_vehicles_fnc_swapVehicle

**Description:** Swaps a vehicle with another vehicle type. Transfers damage, vehicle inventory cargo, and ACE cargo. Takes 20 seconds, requires the player to be an engineer, and the vehicle must be empty. Note: Does not transfer turret magazines - vehicle will need to be rearmed after swap.  

**Arguments:**
- `_vehicle` - The vehicle to swap
- `_player` - The player performing the swap
- `_swapTarget` - The classname of the vehicle to swap to

**Return Value:** None  

**Example:**
```

(begin example)
[cursorTarget, player] call mti_vehicles_fnc_swapVehicle;
(end)

```

**Author:** Ramsey 

