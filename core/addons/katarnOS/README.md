mti_katarnOS
===================

Contains functionality associated with Katarn-class Commando Armour.

# KatarnOS Systems - Developer's Information

## Introduction

This document contains information on making your own equipment compatible with the KatarnOS functions without directly inheriting from the base Commando gear supplieed by MokTech Industries - Armoury.

## Uniforms

The uniform is the heart of the entire system, without a KatarnOS-compatible uniform equipped, most of the functions won't work.

### Implementation Example

```sqf
class CfgWeapons {
    class baseUniformClass;
    class TAG_yourUniformClass: baseUniformClass {
        // ...
        mti_katarnos_isSuit         = 1;        // indicates, that this uniform is KatarnOS-compatible (values: 0/1)
        mti_katarnos_hasOS          = 1;        // indicates, that this uniform comes equipped with the KatarnOS (values: 0/1)
        mti_katarnos_hasTaser       = 1;        // indicates, that this uniform comes equipped with a wrist-plate taser (values: 0/1)
        mti_katarnos_commandoID     = "XX";     // sets the commando's unique ID, displayed in the KatarnOS Team Panel (values: any two-character string)
    };
};
```

## Backpacks

The backpacks have several role-oriented functions, which can be additionally controlled/deactivated through the relevant config properties.

### Implementation Example

```sqf
class CfgVehicles {
    class baseBackpackClass;
    class TAG_yourBackpackClass: baseBackpackClass {
        mti_katarnos_isBackpack     = 1;    // indicates, that this backpack is KatarnOS-compatible (values: 0/1)
        mti_katarnos_hasBeacon      = 1;    // enables the backpack-integrated emergency beacon (values: 0/1)
        mti_katarnos_hasSquadShield = 1;    // enables the backpack-integrated squad shield (values: 0/1)
    };
};
```

## Helmets

The helmets add the KatarnOS HUD and also the intercom and helmet cameras (not explicitly KatarnOS, but covered here for the sake of convenience).

### Implementation Example

```sqf
class CfgWeapons {
    class baseHelmetClass;
    class TAG_yourHelmetClass: baseHelmetClass {
        mti_katarnOS_isHelmet           = 1; // indicates, that this helmet is KatarnOS_compatible (values: 0/1)
        mti_katarnOS_isHUD              = 1; // adds the HUD emitter to this helmet (values: 0/1)
        mti_intercom_hasIntercom        = 1; // adds the intercom system to this helmet (values: 0/1)
        mti_catTabe_core_hasHelmetCam   = 1; // adds the integrated helmet cam to this helmet (values: 0/1)
    };
};
```

## Vests

The vest is primarily responsible for the shield emitters. Although the shields are derived from the Pangolin addon in MokTech, their bindings are included here to the sake of convenience.

### Implementation Example

```sqf
class CfgWeapons {
    class baseVestClass;
    class TAG_yourVestClass: baseVestClass {
        mti_pangolin_hasShield = 1; // adds the Pangolin shield emitters to this vest (values: 0/1)
        mti_pangolin_shieldStrength = 100; // defines the base strength of the shield (values > 0)
        mti_pangolin_shieldRegen = 10; // the base regen rate for the shield in strength/second (values > 0)
        mti_pangolin_regenTimeoutMod = 1; // modifier for the shield timeout after receiving damage before recharging (values >= 1)
    };
};
```

## NVGs

The NVGs add the low-light mode to enhance a commando's vision in dim light conditions.

### Implementation Example

```sqf
class CfgWeapons {
    class baseNVGClass;
    class TAG_yourNVGClass: baseNVGClass {
        mti_katarnOS_isNV = 1; // enables access to the low-light mode for this NVG (values: 0/1)
    };
};
```

