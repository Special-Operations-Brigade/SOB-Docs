# Config Properties

## mti_weapons_core_isImprovMag

- **Value:** Number (Bool)
- **Config Type:** `CfgMagazines`
- **Description:** If set to 1, magazine can be used to improvise ammo in the field.

## mti_weapons_core_isDual

- **Value:** Number (Bool)
- **Config Type:** `CfgWeapons`
- **Description:** Marks affected weapons as compatible with the dual muzzle scripted framework

## mti_weapons_core_is15sRecharge

- **Value:** Number (Bool)
- **Config Type:** `CfgMagazines`
- **Description:** Magazines with this property set to 1 will slowly recharge their ammo using the DC-15s scripted recharge framework

## mti_weapons_core_addLinkedItems

- **Value:** Number (Bool)
- **Config Type:** `CfgWeapons`
- **Description:** Weapons with this property set to 1 will have their linked items and magazine added to the weapon if they newly picked it up. Used to handle ARC Pistol attachments missing after swapping between duals and single pistol with ACE Extended Arsenal.

## mti_weapons_core_canAirburst

- **Value:** Number (Bool)
- **Config Type:** `CfgAmmo`
- **Description:** Marks this ammo as compatible with the airburst munitions framework.

## mti_weapons_core_airBurstAmmo

- **Value:** Text
- **Config Type:** `CfgAmmo`
- **Description:** Class in CfgAmmo which gets released by the airburst munition.

## mti_weapons_core_airburstSecondaries

- **Value:** Number (Bool)
- **Config Type:** `CfgAmmo`
- **Description:** Enables small secondary explosions upon triggering the airburst ammo.

## mti_weapons_core_forceMuzzle

- **Value:** Text
- **Config Type:** `CfgWeapons`
- **Description:** Class reference to attachment in CfgWeapons which should get forcefully added to unit's primary weapons. Used to force the DC-15LE muzzle to stay on the gun permanently.

## mti_weapons_core_forceWalk

- **Value:** Number (Bool)
- **Config Type:** `CfgWeapons`
- **Description:** Weapons with this property set to 1 will render units unable to sprint and run when equipped. Used to control pace for players carrying the NT-242.

## mti_weapons_core_isDroidAttackFlare

- **Value:** Number (Bool)
- **Config Type:** `CfgMagazines`
- **Description:** Used to mark magazines as handheld flare launcher.

## mti_weapons_core_flareType

- **Value:** Text
- **Config Type:** `CfgMagazines`
- **Description:** Class reference in CfgAmmo of type of flare to spawn.

## mti_weapons_core_flareTypeMiddle

- **Value:** Text
- **Config Type:** `CfgMagazines`
- **Description:** Class reference in CfgAmmo of type of flare to spawn. Used by the Droid Attack flare for the center flare.

## mti_weapons_core_isEmergencyFlare

- **Value:** Number (Bool)
- **Config Type:** `CfgMagazines`
- **Description:** Used to mark magazines as handheld flare launcher.

## mti_weapons_core_isHalothane

- **Value:** Number (Bool)
- **Config Type:** `CfgAmmo`
- **Description:** Ammo with this property set to 1 will trigger the spawn of a halothane filled area around them on hit.

## mti_weapons_core_isHuntIR

- **Value:** Number (Bool)
- **Config Type:** `CfgMagazines`
- **Description:** Used to mark magazines as handheld HuntIR launcher.

## mti_weapons_core_huntIRType

- **Value:** Number (Bool)
- **Config Type:** `CfgMagazines`
- **Description:** Used to change the type of IR round to spawn from handheld HuntIR launchers, defaults to the default ACE HuntIR

## mti_weapons_core_railStrength

- **Value:** Number
- **Config Type:** `CfgAmmo`
- **Description:** This property controls the effective strength of rail shot rounds against vehicles.

## mti_weapons_core_crateType

- **Value:** Text
- **Config Type:** `CfgAmmo`
- **Description:** This property controls which resupply crate is spawned with the droppod ammo type.

## mti_weapons_core_ammoType

- **Value:** Number (Enum)
    - `AMMOTYPE_NONE` = 0
    - `AMMOTYPE_STUN` = 1
    - `AMMOTYPE_ION` = 2
    - `AMMOTYPE_RAGDOLL` = 3
    - `AMMOTYPE_MEDICAL` = 4
    - `AMMOTYPE_TRACKING` = 5
    - `AMMOTYPE_ACID` = 6
    - `AMMOTYPE_HACKSHOT` = 7
    - `AMMOTYPE_RAIL` = 8
    - `AMMOTYPE_BEANBAG` = 9
    - `AMMOTYPE_DEFIB` = 10
    - `AMMOTYPE_DROPPOD` = 11
    - `AMMOTYPE_FIRE` = 12
- **Config Type:** `CfgAmmo`
- **Description:** This enum controls the scripted behaviour of special ammo.

## mti_weapons_core_isShadowVirus

- **Value:** Number (Bool)
- **Config Type:** `CfgAmmo`
- **Description:** Ammo with this property set to 1 will trigger the spawn of an area filled with shadow virus around them on hit.

## mti_weapons_core_recharge

- **Value:** Number (Bool)
- **Config Type:** `CfgMagazines`
- **Description:** Magazines with this property set to 1 will slowly recharge over time using the self-recharging stun/ion magazine framework.
