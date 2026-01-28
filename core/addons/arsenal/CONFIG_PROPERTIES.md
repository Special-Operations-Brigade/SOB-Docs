# Config Properties

## mti_armoury_type

- **Value:** Number (Enum)
- **Config Type:** `CfgVehicles`
- **Description:** Allows `this` vehicle to be set up as an armoury object. Value should be one of:
    - 1: Trooper
    - 2: ARC
    - 3: Commando
    - 4: Pilot
    - 5: Cov-Ops
    - 6: Field Support
    - 7: Jump Trooper
    - 99: Command

## mti_arsenal_preset

- **Value:** String
- **Config Type:** `CfgVehicles`
- **Description:** Controls which arsenal whitelist should be made available from `this` object.

## mti_arsenal_whitelists

- **Value:** Array
- **Config Type:** `CfgGlasses`, `CfgMagazines`, `CfgWeapons`, or `CfgVehicles`
- **Description:** Adds `this` item/thing to the given arsenal whitelists. Entries here need to exist in the root config class `mti_arsenal_whitelists` to be parsed correctly.
