# Function Reference

## fnc_addActions.sqf

No documentation available.

## mti_fortify_fnc_addActionToObject

**Description:** Adds action to remove and edit object after it was deployed.  

**Arguments:**
- `_container` - Container the objects was deployed from
- `_preset` - Preset the object was deployed from
- `_object` - The object itself

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_addActionToObject;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_addContainerActions

**Description:** Adds ace interactions to container.  

**Arguments:**
- `_container` 
- `_preset` 

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_addContainerActions;
(end)

```

**Author:** Mokka */  params ["_container","_preset"]; TRACE_2("containerActions",_container,_preset);  if (_container isEqualTo ACE_player) exitWith {};  private _actionList = _container getVariable "ace_interact_menu_actions"; if (isNil "_actionList") then { _actionList = []; };  // gonna remove this for now, just gotta take care of proper main action in the container config itself /* private _mainNode = [_actionList, ["ACE_MainActions"]] call ace_interact_menu_fnc_findActionNode;  TRACE_1("mainNode",_mainNode);  if (isNil {_mainNode}) then { TRACE_1("No Main Action on object", _container);  private _mainAction = [ "ACE_MainActions", "Interactions", "", {}, {true}, nil,nil,nil, 10 ] call ace_interact_menu_fnc_createAction;  private _jipID = [QEGVAR(common,ace_addActionToObject),[_container,0,[],_mainAction]] call CBA_fnc_globalEventJIP; [_jipID,_container] call CBA_fnc_removeGlobalEventJIP; // todo: may have to move this to server exec?! };  */  private _parentAction = [_actionList,[QGVAR(parentAction)]] call ace_interact_menu_fnc_findActionNode;  TRACE_1("parentAction",_parentAction);  if (isNil {_parentAction}) then { _parentAction = [ QGVAR(parentAction), "Fortify", "", // icontodo {}, { params ["_target", "_player", "_args"];  private _canFortify = [_player] call FUNC(canFortify); TRACE_1("can fortify?",_canFortify);  (_canFortify) }, nil,nil,nil, 10 ] call ace_interact_menu_fnc_createAction;  private _jipID = [QEGVAR(common,ace_addActionToObject),[_container,0,["ACE_MainActions"],_parentAction]] call CBA_fnc_globalEventJIP; [_jipID,_container] call CBA_fnc_removeGlobalEventJIP; // todo: may have to move this to server exec?! };  private _presetAction = [_actionList,[format[QGVAR(presetAction_%1),_preset]]] call ace_interact_menu_fnc_findActionNode;  TRACE_1("presetAction",_presetAction);  if (isNil {_presetAction}) then { private _displayName = getText (([_preset] call FUNC(getPresetConfig)) >> "displayName");  _presetAction = [ format[QGVAR(presetAction_%1),_preset], _displayName, "", // icontodo {}, { params ["_target", "_player", "_args"]; _args params ["_container","_preset"];  private _deployedObjects = _container getVariable [(format[QGVAR(deployedObjects_%1),_preset]),[]]; private _total = 0; { _total = _total + (_y select 0); } forEach _deployedObjects;  TRACE_2("has objects?",_preset,_total);  (_total > 0) }, {}, [_container,_preset,_displayName], nil, 10, nil, { params ["_target", "_player", "_args", "_actionData"]; _args params ["_container", "_preset", "_displayName"];  private _budget = [_container, _preset] call FUNC(getBudget); if (_budget >= 0) then { _displayName = format ["%1 (%2)",_displayName,_budget]; };  _actionData set [1, _displayName]; } ] call ace_interact_menu_fnc_createAction;  private _jipID = [QEGVAR(common,ace_addActionToObject),[_container,0,["ACE_MainActions",QGVAR(parentAction)],_presetAction]] call CBA_fnc_globalEventJIP; [_jipID,_container] call CBA_fnc_removeGlobalEventJIP; // todo: may have to move this to server exec?!  private _recallAction = [ "recallAll", "Recall All Objects", "", // icontodo {_this call FUNC(recallAllObjects)}, {true}, {}, [_container,_preset], nil, 10 ] call ace_interact_menu_fnc_createAction;  _jipID = [QEGVAR(common,ace_addActionToObject),[_container,0,["ACE_MainActions",QGVAR(parentAction),format[QGVAR(presetAction_%1),_preset]],_recallAction]] call CBA_fnc_globalEventJIP; [_jipID,_container] call CBA_fnc_removeGlobalEventJIP; // todo: may have to move this to server exec?!  /* todo: figure out any additional actions I might want here... ideas: - highlight objects deployed from this container 

## fnc_addDeployHandler.sqf

No documentation available.

## fnc_addPostDeployHandler.sqf

No documentation available.

## mti_fortify_fnc_addPresetActions

**Description:** Adds child actions to the presets for each object.  

**Arguments:**
- Parent action arguments

**Return Value:** Preset child actions  

**Example:**
```

(begin example)
[...] call mti_fortify_fnc_addPresetActions;
(end)

```

**Author:** Mokka 

## fnc_axisLengths.sqf

No documentation available.

## fnc_buildLocationModule.sqf

No documentation available.

## mti_fortify_fnc_canCreateFOBMarker

**Description:** Checks whether an FOB marker can be deployed from given object.  

**Arguments:**
- `_player` 
- `_target` 

**Return Value:** canCreateFOBMarker?  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_canCreateFOBMarker;
(end)

```

**Author:** Mokka 

## fnc_canFortify.sqf

No documentation available.

## mti_fortify_fnc_canRecallObjectsPlayer

**Description:** Checks whether player has any objects to recall to the backpack.  

**Arguments:**
- `_player` - Player

**Return Value:** canRecallObjects?  

**Example:**
```

(begin example)
[ace_player] call mti_fortify_fnc_canRecallObjectsPlayer;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_compositionDeployCanceled

**Description:** Resets values after composition deploy was cancelled.  

**Arguments:**
- ...

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_compositionDeployCanceled;
(end)

```

**Author:** Mokka 

## fnc_compositionDeployConfirm.sqf

No documentation available.

## mti_fortify_fnc_compositionDeployFinished

**Description:** Handles placing the composition after placement, runs post-deploy handlers and triggers events.  

**Arguments:**
- ...

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_compositionDeployFinished;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_compositionPlaced

**Description:** Handles composition being placed, server-side broadcast  

**Arguments:**
- `_unit` - Unit that placed the composition
- `_container` - Container the composition was deployed from
- `_objects` - The objects of the composition
- `_marker` - Marker as string, empty if no marker should be created
- `_posASL` - Center position of the composition
- `_cost` - Cost of the composition

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_compositionPlaced;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_createFOBMarker

**Description:** Creates a FOB marker on the given target's position.  

**Arguments:**
- `_player` 
- `_target` 

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_createFOBMarker;
(end)

```

**Author:** Mokka 

## fnc_createObjectMarker.sqf

No documentation available.

## mti_fortify_fnc_deleteFOBMarker

**Description:** Delete the FOB marker of the given target.  

**Arguments:**
- `_player` 
- `_target` 

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_deleteFOBMarker;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_deployCanceled

**Description:** Resets values if deployment was canceled  

**Arguments:**
- ...

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_deployCanceled;
(end)

```

**Author:** Mokka 

## fnc_deployComposition.sqf

No documentation available.

## fnc_deployConfirm.sqf

No documentation available.

## mti_fortify_fnc_deployFinished

**Description:** Deploys the object after placement, runs post-deploy handlers and triggers events  

**Arguments:**
- ...

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_deployFinished;
(end)

```

**Author:** Mokka 

## fnc_deployObject.sqf

No documentation available.

## mti_fortify_fnc_exportComposition

**Description:** Exports the given composition to clipboard.  

**Arguments:**
- `_name` - Name to use on export
- `_data` - Composition data

**Return Value:** Composition in string format  

**Example:**
```

(begin example)
[ace_player] call mti_fortify_fnc_exportComposition;
(end)

```

**Author:** Mokka */  params ["_name", "_data"];  private _br = toString [13, 10]; private _tab = toString [9]; private _output = format ["/*%1Composition Export:%1%2Name: %3%1%2Cost: %4%1 

## mti_fortify_fnc_getAvailablePresets

**Description:** Returns available presets/containers in area (and from backpack)  

**Arguments:**
- `_player` - Player to check presets for

**Return Value:** Entries in format [_classname, _container, _totalBudget]  

**Example:**
```

(begin example)
[ACE_player] call mti_fortify_fnc_getAvailablePresets;
(end)

```

**Author:** Mokka 

## fnc_getBudget.sqf

No documentation available.

## fnc_getCompositionBudget.sqf

No documentation available.

## mti_fortify_fnc_getCompositionConfig

**Description:** Helper function to get config path to given composition.  

**Arguments:**
- `_composition` - Composition

**Return Value:** Config Path  

**Example:**
```

(begin example)
["Example_Composition"] call mti_fortify_fnc_getCompositionConfig;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_getContainerPresets

**Description:** Returns a hashmap of all the given containers presets and the attached budget.  

**Arguments:**
- `_container` - Container to return presets for (object or class name)

**Return Value:** Hashmap with container's presets as key and budgets as values  

**Example:**
```

(begin example)
[cursorTarget] call mti_fortify_fnc_getContainerPresets;
(end)

```

**Author:** Mokka 

## fnc_getCost.sqf

No documentation available.

## mti_fortify_fnc_getObjectCount

**Description:** Returns how often given object has already been deployed from a container.  

**Arguments:**
- `_container` 
- `_preset` 
- `_typeOf` 

**Return Value:** None  

**Example:**
```

(begin example)
[cursorTarget, "Example_Preset", "Sandbag"] call mti_fortify_fnc_getObjectCount;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_getPresetConfig

**Description:** Helper function to get config path to given preset.  

**Arguments:**
- `_preset` - Preset

**Return Value:** Config Path  

**Example:**
```

(begin example)
["Example_Preset"] call mti_fortify_fnc_getPresetConfig;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_getPresetObjects

**Description:** Returns all of a preset's objects, costs and limits  

**Arguments:**
- `_preset` - The preset

**Return Value:** All preset's objects, budgets and limits  

**Example:**
```

(begin example)
["Example_Preset"] call mti_fortify_fnc_getPresetObjects;
(end)

```

**Author:** Mokka 

## fnc_handleChatCommand.sqf

No documentation available.

## fnc_handleScrollWheel.sqf

No documentation available.

## mti_fortify_fnc_interaction_addCompositionActions

**Description:** Adds composition actions to suitable containers in player's vicinity.  

**Arguments:**
- `_interactionType` - 0, world / 1, self

**Return Value:** None  

**Example:**
```

(begin example)
[0] call mti_fortify_fnc_interaction_addCompositionActions;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_interaction_addSaveActions

**Description:** Adds save/load composition actions to suitable containers in player's vicinity.  

**Arguments:**
- `_interactionType` - 0, world / 1, self

**Return Value:** None  

**Example:**
```

(begin example)
[0] call mti_fortify_fnc_interaction_addSaveActions;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_loadComposition

**Description:** Handles loading a composition from a save container.  

**Arguments:**
- ACE Action Arguments

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_fortify_fnc_loadComposition;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_manageSavedCompositions

**Description:** Handles the dialog to rename/remove saved compositions.  

**Arguments:**
- None

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_manageSavedCompositions;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_objectPlaced

**Description:** Handles object being placed, server broadcast  

**Arguments:**
- `_unit` - Unit that placed the object
- `_container` - The container the object was deployed from
- `_preset` - Class-name of the preset the object was from
- `_object` - The object that was placed

**Return Value:** None  

**Example:**
```

(begin example)
[] call mti_fortify_fnc_objectPlaced;
(end)

```

**Author:** Mokka 

## mti_fortify_fnc_objectsGrabber

**Description:** Helper function to grab nearby objects and save them in format compatible with mti_fortify_fnc_objectsMapper. Grabbed objects are also exported to clipboard for quick saving.  

**Arguments:**
- `_pos` - Center position
- `_radius` - Radius
- `_outputName` - (optional) name of the saved composition, shown in output text

**Return Value:** Nearby objects in format [classname, relative position, azimuth, vector up, cost(, init)]  

**Example:**
```

(begin example)
[position ACE_player,150] call mti_fortify_fnc_objectsGrabber;
(end)

```

**Author:** Mokka */  params [["_pos",[0,0,0],[[]]], ["_radius",0,[0]], ["_name", ""]];  private _objects = [];  private _br = toString [13, 10]; private _tab = toString [9]; private _output = format ["/*%1objectGrabber Output:%1Name: %2%1 

## fnc_objectsMapper.sqf

No documentation available.

## mti_fortify_fnc_recallAllCompositions

**Description:** Recalls all objects deployed from given container through compositions.  

**Arguments:**
- action args

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_fortify_fnc_recallAllCompositions;
(end)

```

**Author:** Mokka */  /* todo: figure out if we want to limit the range of the recall?! e.g. only objects within 100m can be recalled using this.... 

## mti_fortify_fnc_recallAllObjects

**Description:** Recalls all preset objects deployed from given container, returning budget.  

**Arguments:**
- action args

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_fortify_fnc_recallAllObjects;
(end)

```

**Author:** Mokka */  /* todo: figure out if we want to limit the range of the recall?! e.g. only objects within 100m can be recalled using this.... 

## mti_fortify_fnc_recallAllObjectsPlayer

**Description:** Recalls all objects placed from player backpack  

**Arguments:**
- `_player` - Player

**Return Value:** None  

**Example:**
```

(begin example)
[ace_player] call mti_fortify_fnc_recallAllObjectsPlayer;
(end)

```

**Author:** Mokka */  /* todo: figure out if we want to limit the range of the recall?! e.g. only objects within 100m can be recalled using this.... 

## mti_fortify_fnc_saveComposition

**Description:** Handles saving nearby deployed objects into a composition  

**Arguments:**
- ACE Action Arguments

**Return Value:** None  

**Example:**
```

(begin example)
[...] call mti_fortify_fnc_saveComposition;
(end)

```

**Author:** Mokka 

## fnc_updateBudget.sqf

No documentation available.

## fnc_updateCompositionBudget.sqf

No documentation available.

## mti_fortify_fnc_updateObjectCount

**Description:** Updates deployedObjects variable on the container.  

**Arguments:**
- `_container` 
- `_preset` 
- `_object` 
- `_change` 

**Return Value:** None  

**Example:**
```

(begin example)
[containerA, "Example_Preset", "Sandbag", +1] call mti_fortify_fnc_updateObjectCount;
(end)

```

**Author:** Mokka 

