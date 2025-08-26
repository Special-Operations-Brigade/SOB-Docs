# Function Reference

## mti_logistics_fnc__itemsFromArsenal

**Description:** Compiles an updated list of items based on the arsenal whitelists, to be used for cfg/items.hpp Requires the ConfigDumpFileIO extension to be loaded manually, it is not included in the mod release, see mti_common_fnc_dumpConfig for details.  

**Arguments:**
- None

**Return Value:** None (written to file items.hpp in main Arma 3 directory)  

**Example:**
```

(begin example)
[] call mti_logistics_fnc__itemsFromArsenal;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_dialogPFH

**Description:** PFH that runs some recurring checks on the logibox dialog.  

**Arguments:**
- `_display` - Display reference
- `_logibox` - LogiBox reference

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_dialogPFH;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_aircraft_onLoad

**Description:** Handles setting up the display, populating it with data and getting everything ready when the aircraft logibox menu is opened.  

**Arguments:**
- `_display` - Display reference

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_aircraft_onLoad;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_aircraft_onUnload

**Description:** Handles resetting variables and systems when the aircraft logibox menu gets closed.  

**Arguments:**
- `_display` - Display reference
- `_exitCode` - Exit code thrown by the display

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_aircraft_onUnload;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_aircraft_updateDialog

**Description:** Updates the LogiBox dialog based on currently selected vehicle.  

**Arguments:**
- `_listBoxVehicle` - Vehicle listbox ctrl
- `_curSel` - Current selection

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_aircraft_updateDialog;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_canOpenDialog

**Description:** Checks whether player can currently open the logibox menu.  

**Arguments:**
- `_logibox` - LogiBox reference

**Return Value:** canOpenDialog?  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_canOpenDialog;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_clearArea

**Description:** Clears the output area of the logibox.  

**Arguments:**
- `_ctrl` - Ctrl

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_clearArea;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_getConfigProperty

**Description:** Helper function to properly retrieve properties from the logistics config  

**Arguments:**
- `_config` - Config class to retrieve config from (if array, path)
- `_class` - Class name to look up
- `_property` - Property to retrieve

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_getConfigProperty;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_getDeployed

**Description:** Gets the number of deployed vehicles for a given logibox and vehicle.  

**Arguments:**
- `_logibox` - The logibox object
- `_class` - The vehicle class name

**Return Value:** The number of deployed vehicles.  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_getDeployed;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_getLimit

**Description:** Returns the applicable spawning limit (if any) for the corresponding vehicle class.  

**Arguments:**
- `_logibox` - LogiBox reference
- `_type` - type of logibox (if array, config path)
- `_class` - Classname of the vehicle to look up

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_getLimit;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_handleSlingload

**Description:** Handles the logibox getting picked up by a LAAT/c (hiding/unhiding the helpers)  

**Arguments:**
- `_ehArgs` - The args passed as part of the event
- `_args` - The args passed directly from the event handler (the logibox object)
- `_id` - The ID of the eh
- `_type` - The type of the eh, to differentiate behaviour

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_handleSlingload;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_limitHashDialog

**Description:** Opens a dialog that allows the user to set limits for vehicle deployment.  

**Arguments:**
- `_logibox` - The logibox object

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_limitHashDialog;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_logibox_checkArea

**Description:** Checks the helper area next to the logibox, if anything is blocking the output.  

**Arguments:**
- `_logibox` - LogiBox reference
- `_positions` - Helper centre position and bounding box lengths
- `_helper` - The helper visual object

**Return Value:** If area is clear  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_logibox_checkArea;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_logibox_init

**Description:** Handles local initilization for the logibox.  

**Arguments:**
- `_logibox` - LogiBox reference

**Return Value:** If area is clear  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_logibox_init;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_openDialog

**Description:** Wrapper function to open desired logibox dialog.  

**Arguments:**
- `_logibox` - Logibox reference

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_openDialog;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_spawnVehicle

**Description:** Server-side spawning the vehicle and setting various timers on the logibox.  

**Arguments:**
- `_mode` - 1 for aircraft, 2 for vehicles
- `_logibox` - The logibox
- `_selectedVehicle` - Vehicle to spawn
- `_selectedSkin` - Skin that was selected, "" if using default
- `_configureLoadout` - If vehicle loadout should be adjusted after spawning (aircraft only)
- `_orientation` - The orientation of the new vehicle (in cardinal direction degrees)
- `_player` - Player that initiated the spawn

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_spawnVehicle;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_spawnVehicleComplete

**Description:** Takes care of the actual spawning of the vehicle once all the fancy visual stuff is done.  

**Arguments:**
- `_mode` - 1 for aircraft, 2 for vehicles
- `_logibox` - The logibox
- `_selectedVehicle` - Vehicle to spawn
- `_selectedSkin` - Skin that was selected, "" if using default
- `_configureLoadout` - If vehicle loadout should be adjusted after spawning (aircraft only)
- `_orientation` - Orientation to spawn the vehicle in (in cardinal direction degrees)
- `_player` - Player that initiated the spawn

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_spawnVehicleComplete;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_updateScreenDisplay

**Description:** Updates the screen UI of the given logibox  

**Arguments:**
- `_logibox` - The logibox
- `_display` - The screen display

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_updateScreenDisplay;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_updateVehLb

**Description:** Updates the vehicle listbox for the logibox menu.  

**Arguments:**
- `_display` - Display reference
- `_logibox` - LogiBox reference

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_updateVehLb;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_vehicle_dialogPFH

**Description:** PFH that runs some recurring checks on the logibox dialog.  

**Arguments:**
- `_display` - Display reference
- `_logibox` - LogiBox reference

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_dialogPFH;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_vehicle_onLoad

**Description:** Handles setting up the display, populating it with data and getting everything ready when the vehicle logibox menu is opened.  

**Arguments:**
- `_display` - Display reference

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_vehicle_onLoad;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_vehicle_onUnload

**Description:** Handles resetting variables and systems when the vehicle logibox menu gets closed.  

**Arguments:**
- `_display` - Display reference
- `_exitCode` - Exit code thrown by the display

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_vehicle_onUnload;
(end)

```

**Author:** Mokka 

## mti_logistics_fnc_vehicle_updateDialog

**Description:** Updates the LogiBox dialog based on currently selected vehicle.  

**Arguments:**
- `_listBoxVehicle` - Vehicle listbox ctrl
- `_curSel` - Current selection

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_logistics_fnc_vehicle_updateDialog;
(end)

```

**Author:** Mokka 

