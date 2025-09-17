# Function Reference

## mti_tpw_fnc_bcLoaded

**Description:** Checks if BCs Primaries is Loaded  

**Arguments:**
- `_unit` - Client

**Return Value:** Bool  

**Example:**
```

(begin example)
[_unit] call mti_tpw_fnc_bcLoaded
(end)

```

**Author:** Chimera 

## mti_tpw_fnc_checkSecondaryWeapon

**Description:** Checks if unit has a bcse tertiary  

**Arguments:**
- `_unit` - Client

**Return Value:** Bool  

**Example:**
```

(begin example)
[_unit] call mti_tpw_fnc_bcseStatus;
(end)

```

**Author:** Chimera 

## mti_tpw_fnc_getPrimary

**Description:** Retrieves Primary Weapon name  

**Arguments:**
- `_unit` - client

**Return Value:** String  

**Example:**
```

(begin example)
[_unit] call mti_tpw_fnc_getPrimary;
(end)

```

**Author:** Chimera 

## mti_tpw_fnc_getSecondary

**Description:** Retrieves secondary weapon name  

**Arguments:**
- `_unit` - client

**Return Value:** None  

**Example:**
```

(begin example)
[_unit] call mti_tpw_fnc_getSecondary;
(end)

```

**Author:** Chimera 

## mti_tpw_fnc_isBCweapon

**Description:** Checks if secondary weapon is from BCs  

**Arguments:**
- `_unit` - client

**Return Value:** Bool  

**Example:**
```

(begin example)
[_unit] call mti_tpw_fnc_isBCweapon;
(end)

```

**Author:** Chimera 

