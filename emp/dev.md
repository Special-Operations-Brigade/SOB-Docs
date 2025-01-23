# MTI EMP - Dev Info

- [MTI EMP - Dev Info](#mti-emp---dev-info)
  - [Introduction](#introduction)
  - [EMP Damage](#emp-damage)
    - [Implementation Example](#implementation-example-1)
  - [EMP Resistance](#emp-resistance)
    - [Implementation Example](#implementation-example-2)
  - [Equipment Scrambling](#equipment-scrambling)
    - [Implementation Example](#implementation-example-3)
  - [Field Servicing Kit](#field-servicing-kit)
    - [Implementation Example](#implementation-example-3)

## Introduction

This document serves as a comprehensive guide to MokTech's custom EMP damage system, as well as how it can be incoperated on new weapons or equipment.

## EMP Damage 

The MTI EMP system uses a uniquely coded damage system to detect, calculate and afflict EMP-based damage onto entities and vehicles. This damage is stored in a weapon's ammo class instead of the weapon itself, in `baseEmpDamage`.

Explosive based EMP munitions additionally require `innerRadius` and `maxRadius` to function as intended. Entities/objects within the `innerRadius` experience no damage falloff after resistance mitigation. `maxRadius` entities take progressively less damage the farther away from the origin they are.

### Implementation Examples

```sqf
class CfgoAmmo {
    class baseAmmoClass;
    class TAG_yourAmmoClass: baseAmmoClass {
        ...

        mti_emp_baseEmpDamage = 1;    // an integer value that determines base (unmitigated) damage. (value 1-x)
        mti_emp_innerRadius = 1;      // (explosive) an interger value that determines immediate effective range. (value 1-x)
        mti_emp_maxRadius = 1;        // (explosive) an integer value that determines maximum effective range. (value 1-x)
    };
};
```

## EMP Resistance

Entities/vehicles have `empResistance`. If `baseEmpDamage` is less than or equal to the resistance of the object, no damage processing is done. If the EMP's damage is `2 x empResistance`, the object damage will be set to `1` without further processing.

Vehicles specifically have unique damage processing, in that damage is instead mapped randomly onto a set of pre-determined core instruments. If a vehicle, who has `hitEngine`, sustaints >=90% damage on that hitpoint, it will have it's turrets (*if applicable*) disabled.

### Implementation Examples

```sqf
class CfgVehicles {
    class baseUnitClass;
    class TAG_yourUnitClass: baseUnitClass {
        ...

        mti_emp_empResistance = 1;    // an integer value that determines how resistant a vehicle is. (value 1-x)
    };
};
```

## Equipment Scrambling

Units of `CAManBase` hit by EMPs strong enough (*150 base*) have the added risk of having equipment or instruments fried. By default, units have a 1/4 chance of triggering an instrument fry. Randomly, the unit's `map`, `gps`, `nvg` or `radio` are unassigned from the item slot.

### Implementation Examples

```sqf

_unit

[_unit] call MTI_emp_fnc_scrambleInstruments;
```

## Field Servicing KIt

To repair instruments or armor damaged by EMP blasts through `scrambleInstruments`, MTI provides a Field Service Kit. Field Service Kits, upon use, will completely restore all instrument functionality.

```sqf

_unit

[_unit] call MTI_emp_fnc_repairInstruments;
```