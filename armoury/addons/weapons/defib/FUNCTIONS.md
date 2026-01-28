# Function Reference

## mti_armoury_weapons_defib_fnc_fired

**Description:** Handles events after the defib was fired.  

**Arguments:**
- `_unit` - Unit that fired
- `_weapon` - Weapon that was fired
- `_muzzle` - Muzzle that was fired
- `_mode` - Current weapon mode
- `_ammo` - Ammo that was fired
- `_magazine` - Current magazine
- `_projectile` - Fired projectile

**Return Value:** None  

**Example:**
```

(begin example)
class EventHandlers {
fired = "_this call mti_armoury_weapons_defib_fnc_fired";
};
(end)

```

**Author:** Mokka 

