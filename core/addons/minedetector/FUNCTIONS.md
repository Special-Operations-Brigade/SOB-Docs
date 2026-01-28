# Function Reference

## mti_minedetector_fnc_activateDetector

**Description:** Activate the mine detector  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_minedetector_fnc_activateDetector
(end)

```

**Author:** Glowbal, Mokka 

## mti_minedetector_fnc_canActivateDetector

**Description:** Check if mine detector can be activated  

**Arguments:**
- None

**Return Value:** If mine detector can be activated  

**Example:**
```

(begin example)
[] call mti_minedetector_fnc_canActivateDetector
(end)

```

**Author:** Glowbal, Mokka 

## mti_minedetector_fnc_canDeactivateDetector

**Description:** Check if mine detector can be deactivated  

**Arguments:**
- None

**Return Value:** If mine detector can be deactivated  

**Example:**
```

(begin example)
[] call mti_minedetector_fnc_canDeactivateDetector
(end)

```

**Author:** Glowbal, Mokka 

## mti_minedetector_fnc_deactivateDetector

**Description:** Deactivate the mine detector  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_minedetector_fnc_deactivateDetector
(end)

```

**Author:** Glowbal, Mokka 

## mti_minedetector_fnc_detectorLoop

**Description:** Handle mine detection in a PFH loop  

**Arguments:**
- `_args` - PFH args array
- `_pfhID` - ID of the PFH for removal

**Return Value:** None  

**Example:**
```

(begin example)
[[...], 2] call mti_minedetector_fnc_detectorLoop
(end)

```

**Author:** Glowbal, Mokka 

## mti_minedetector_fnc_disableDetector

**Description:** Disables the mine detector  

**Arguments:**
- `_unit` - Unit
- `_detectorType` - class name of detector

**Return Value:** None  

**Example:**
```

(begin example)
[ACE_Player, "MTI_Detector"] call mti_minedetector_fnc_disableDetector
(end)

```

**Author:** Glowbal, Mokka 

## mti_minedetector_fnc_enableDetector

**Description:** Enables the mine detector  

**Arguments:**
- `_unit` - Unit
- `_detectorType` - class name of detector

**Return Value:** None  

**Example:**
```

(begin example)
[ACE_Player, "MTI_Detector"] call mti_minedetector_fnc_enableDetector
(end)

```

**Author:** Glowbal, Mokka 

## mti_minedetector_fnc_hasDetector

**Description:** Check if unit has a mine detector  

**Arguments:**
- `_unit` - Unit

**Return Value:** If unit has a mine detector  

**Example:**
```

(begin example)
[ace_player] call mti_minedetector_fnc_hasDetector
(end)

```

**Author:** Glowbal, Mokka 

