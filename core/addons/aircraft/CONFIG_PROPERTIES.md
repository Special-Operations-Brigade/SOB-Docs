# Config Properties

## mti_aircraft_canService

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Used to control if `this` vehicle can service aircraft.

## mti_aircraft_cpas_automaticDetach

- **Value:** Number (Bool)
- **Config Type:** `CfgAmmo`
- **Description:** If enabled, attached CPAS rigs will be automatically detached before the carrier projectile impacts the ground.

## mti_aircraft_cpas_compatible

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Marks `this` vehicle as a CPAS-compatible aircraft.

## mti_aircraft_cpas_isAmmo

- **Value:** Number (Bool)
- **Config Type:** `CfgAmmo`
- **Description:** Marks `this` ammo as CPAS carrier munition.

## mti_aircraft_cpas_isRig

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Used to mark backpacks as CPAS rigs, allowing players wearing packs with this property enabled to attach to loaded CPAS pylons.

## mti_aircraft_cpas_parachuteClass

- **Value:** String (Class in `CfgVehicles`)
- **Config Type:** `CfgVehicles`
- **Description:** Sets the parachute that gets deployed from the CPAS rig after detaching from the carrier projectile.

## mti_aircraft_cpas_pylonOffsets

- **Value:** String (Simple Array)
- **Config Type:** `CfgVehicles`
- **Description:** The string representation of nested arrays containing the `[x,y,z]` offset for each CPAS-compatible pylon.

## mti_aircraft_hasCloaking

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Enables activeCamo cloaking on `this` vehicle.

## mti_aircraft_hasSkins

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Master toggle to inform the dynamic skin selector that `this` vehicles has multiple skins.

## mti_aircraft_hasSmokeLauncher

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Enables the smoke launcher for `this` aircraft. A weapon with the property `mti_aircraft_isSmokeLauncher` is still required.

## mti_aircraft_isSmokeLauncher

- **Value:** Number (Bool)
- **Config Type:** `CfgWeapons`
- **Description:** Marks `this` as an aircraft smoke launcher.

## mti_aircraft_laatc_canBeLoaded

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Used to allow `this` vehicle, object or unit to be loaded by the LAAT/c.

## mti_aircraft_laatc_canLoad

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Enables `this` aircraft to use the LAAT/c mag-clamping script to load other vehicles/objects.

## mti_aircraft_laatc_loadedSize

- **Value:** Number
- **Config Type:** `CfgVehicles`
- **Description:** Defines how much space `this` vehicle should occupy in the LAAT/c's mag-clamps.

## mti_aircraft_laatc_loadVars

- **Value:** String (Simple Array)
- **Config Type:** `CfgVehicles`
- **Description:** String representation of a nested array which contains the `[x,y,z]` offsets for each cargo space and values for hinge and clamp rotation. Eg. `"[[[0,-3.7,-7.8]], [0], [0]]"`.

## mti_aircraft_MissileStrength

- **Value:** Number
- **Config Type:** `CfgAmmo`
- **Description:** Used by the Scalpel Missiles to limit which vehicles are immune to its crew-killing effect, by comparing against the target's armour value.

## mti_aircraft_repairOnly

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`
- **Description:** Marks `this` vehicle as a repair-only facility/servicing vehicle, without refuel or reload capabilities.

## mti_aircraft_scope

- **Value:** Number (Bool)
- **Config Type:** `CfgVehicles`/`class TextureSources`
- **Description:** Used to control the visibility of vehicle skins inside of `class TextureSources` sub-classes of `this` vehicle.

