# Function Reference

## mti_weapons_core_fnc_15sFiredEH

**Description:** Handles setting the recharge delay when the 15s has been fired.  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_15sFiredEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_15sPFEH

**Description:** Per-frame handler to slowly recharge the DC-15s side-arm.  

**Arguments:**
- `_args` - Unused
- `_handle` - PFEH handle

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_15sPFEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_17sARC_LoadoutEH

**Description:** Handles adding accessories after equipping/unequipping the 17s ARC  

**Arguments:**
- `_unit` - Unit to handle
- `_newLoadout` - New loadout (unused)
- `_oldLoadout` - Old loadout (unused)

**Return Value:** None  

**Example:**
```

(begin example)
[ACE_player] call mti_weapons_core_fnc_17sARC_LoadoutEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_17sDual_FiredEH

**Description:** Handles switching between the two guns  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_17sDual_FiredEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_17sDual_LoadoutEH

**Description:** Handles setting ammo values after equipping/unequipping the 17s Dual  

**Arguments:**
- `_unit` - Unit to handle
- `_newLoadout` - New loadout (unused)
- `_oldLoadout` - Old loadout (unused)

**Return Value:** None  

**Example:**
```

(begin example)
[ACE_player] call mti_weapons_core_fnc_17sDual_LoadoutEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_17sDual_ReloadedEH

**Description:** Handles reloading the dual weapons  

**Arguments:**
- `_unit` - Unit that reloaded
- `_weapon` - Weapon that got reloaded
- `_muzzle` - Weapon muzzle that got reloaded
- `_newMagazine` - New magazine info
- `_oldMagazine` - Old magazine

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_17sDual_ReloadedEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_airburst_firedEH

**Description:** Handles releasing airburst munitions after delay has expired.  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_airburst_firedEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_setTimer

**Description:** Handles setting the delay for airburst munitions.  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_weapons_core_fnc_setTimer;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_canImproviseAmmo

**Description:** Checks whether given player can improvise ammo for their current weapon  

**Arguments:**
- `_player` - Player to check

**Return Value:** canImproviseAmmo?  

**Example:**
```

(begin example)
[ace_player] call mti_weapons_core_fnc_canImproviseAmmo;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_check15LEMuzzle

**Description:** Makes sure that DC-15LE has the correct muzzle attachment.  

**Arguments:**
- `_unit` - Unit to check

**Return Value:** None  

**Example:**
```

(begin example)
[ACE_player] call mti_weapons_core_fnc_check15LEMuzzle;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_checkNT242Walk

**Description:** Checks walk state based on NT-242 weapon presence in player's loadout.  

**Arguments:**
- `_unit` - Unit to check
- `_newUnitLoadout` - New loadout of the unit
- `_oldUnitLoadout` - Old loadout of the unit

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_checkNT242Walk;
(end)

```

**Author:** Mokka 

## fnc_createHalothaneTrigger.sqf

No documentation available.

## fnc_createShadowVirusTrigger.sqf

No documentation available.

## mti_weapons_core_fnc_droidAttackFlare_FiredEH

**Description:** Handles launching the droid attack flare  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_droidAttackFlare_FiredEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_emergencyFlare_FiredEH

**Description:** Handles launching the emergency flare  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_emergencyFlare_FiredEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_haad_FiredEH

**Description:** Handles attaching the Health an Ammo Dispenser to the proper Grenade  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_haad_FiredEH;
(end)

```

**Author:** Chimera */  params ["_unit", "_weapon", "_muzzle", "_mode", "_ammo", "_magazine", "_projectile"];  // backlog: emptied func for now /* private _isHAAD = _ammo isKindOf "MTI_ammo_haad";  if (_isHAAD) then { private _vehicle = createVehicle ["mti_haad", getPos _projectile]; _vehicle attachTo [_projectile, [0,0,0]]; _vehicle setVariable [QEGVAR(haad,charges),3,true]; }; 

## mti_weapons_core_fnc_Halothane_firedEH

**Description:** Handles the release of Halothane particles.  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_halothane_firedEH;
(end)

```

**Author:** Arcanist 

## fnc_handleHalothane.sqf

No documentation available.

## fnc_handleHalothaneLocal.sqf

No documentation available.

## fnc_handleShadowVirus.sqf

No documentation available.

## fnc_handleShadowVirusLocal.sqf

No documentation available.

## mti_weapons_core_fnc_handleTracking

**Description:** Description...  

**Arguments:**
- `_` - expl.

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_weapons_core_fnc_handleTracking;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_huntIR_FiredEH

**Description:** Handles launching the handheld huntIR  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_huntIR_FiredEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_improviseAmmo

**Description:** Allows player to improvise some ammo for the Verpine Shatter Rifle.  

**Arguments:**
- `_player` - Player doing the improvising

**Return Value:** None  

**Example:**
```

(begin example)
[ace_player] call mti_weapons_core_fnc_improviseAmmo;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_loadout

**Description:** Loadout EH.  

**Arguments:**
- `_this` - Passed by loadout event

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_weapons_core_fnc_loadout;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_onHit

**Description:** Handles onHit events for units.  

**Arguments:**
- `_target` - passed by EH
- `_shooter` - passed by EH
- `_projectile` - passed by EH
- `_position` - passed by EH
- `_velocity` - passed by EH
- `_selection` - passed by EH
- `_ammo` - passed by EH
- `_vector` - passed by EH
- `_radius` - passed by EH
- `_surfaceType` - passed by EH
- `_isDirect` - passed by EH

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_onHit;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_onHit_Acid

**Description:** Handle unit gettting hit by an acid round. For a specified duration after a unit got hit by a round of this type, the unit's corpse will be "dissolved" after a while.  

**Arguments:**
- `_target` - Unit that got hit
- `_shooter` - Unit that shot the round
- `_ammo` - Class name of the ammo that hit the target

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_onHit_Acid;
(end)

```

**Author:** Crimzonkat, modified by Mokka 

## fnc_onHit_Beanbag.sqf

No documentation available.

## fnc_onHit_Droppod.sqf

No documentation available.

## mti_weapons_core_fnc_onHit_HackShot

**Description:** Handle unit gettting hit by a hacking round.  

**Arguments:**
- `_target` - Unit that got hit
- `_shooter` - Unit that shot the round
- `_ammo` - Class name of the ammo that hit the target

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_onHit_HackShot;
(end)

```

**Author:** Arcanist 

## mti_weapons_core_fnc_onHit_Ion

**Description:** Handle unit gettting hit by an ion round. Modified version of the stun/ion system written by Crimzonkat for Legion Studios.  

**Arguments:**
- `_target` - Unit that got hit
- `_shooter` - Unit that shot the round
- `_ammo` - Class name of the ammo that hit the target

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_onHit_Ion;
(end)

```

**Author:** Crimzonkat, modified by Mokka 

## mti_weapons_core_fnc_onHit_Medical

**Description:** Handle unit gettting hit by a medical round. Administers dose of given meds to the target.  

**Arguments:**
- `_target` - Unit that got hit
- `_shooter` - Unit that shot the round
- `_ammo` - Class name of the ammo that hit the target
- `_bodyPart` - The bodypart that was hit

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_onHit_Medical;
(end)

```

**Author:** Mokka 

## fnc_onHit_RailShot.sqf

No documentation available.

## mti_weapons_core_fnc_onHit_Stun

**Description:** Handle unit gettting hit by a stun round. Modified version of the stun/ion system written by Crimzonkat for Legion Studios.  

**Arguments:**
- `_target` - Unit that got hit
- `_shooter` - Unit that shot the round
- `_ammo` - Class name of the ammo that hit the target

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_onHit_Stun;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_onHit_Tracking

**Description:** Handle unit gettting hit by a tracking round. Will place a tracking marker on player's map that updates with target's position occasionally.  

**Arguments:**
- `_target` - Unit that got hit
- `_shooter` - Unit that shot the round
- `_ammo` - Class name of the ammo that hit the target

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_onHit_Tracking;
(end)

```

**Author:** Crimzonkat, modified by Mokka 

## mti_weapons_core_fnc_shadowVirus_firedEH

**Description:** Handles the release of ShadowVirus particles.  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_shadowVirus_firedEH;
(end)

```

**Author:** Arcanist 

## mti_weapons_core_fnc_stun

**Description:** Handles effects for units getting stunned/ion'd. Modified version of the function written by Crimzonkat for Legion Studios.  

**Arguments:**
- `_target` - The target to handle effects for
- `_duration` - Duration in seconds for the effect to persist for
- `_ammoType` - Ammo type that was used to stun/ion

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_weapons_core_fnc_stun;
(end)

```

**Author:** Crimzonkat, modified by Mokka 

## mti_weapons_core_fnc_stun_FiredEH

**Description:** Handles setting values for recharging the ion and stun cells  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Fired weapon
- `_muzzle` - Used muzzle
- `_mode` - Firemode
- `_ammo` - Ammo used
- `_magazine` - Magazine used
- `_projectile` - Projectile

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_stun_FiredEH;
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_stun_PFEH

**Description:** Handles "recharging" the stun and ion cells  

**Arguments:**
- `_args` - Unused
- `_handle` - PFH handle

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_stun_FPFEH
(end)

```

**Author:** Mokka 

## mti_weapons_core_fnc_stun_UAEH

**Description:** Handles setting ammo count correctly when switching to stun muzzle  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
_this call mti_weapons_core_fnc_stun_UAEH
(end)

```

**Author:** Mokka 

