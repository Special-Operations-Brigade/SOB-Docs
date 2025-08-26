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

