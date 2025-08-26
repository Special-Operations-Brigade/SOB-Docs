sob_equipment
===================

# ToC
- [sob\_equipment](#sob_equipment)
- [ToC](#toc)
- [How 2 Add Textures](#how-2-add-textures)
  - [Differences from v1 to v2](#differences-from-v1-to-v2)
- [Macro Reference](#macro-reference)
  - [Legend](#legend)
  - [ARC](#arc)
    - [MACRO\_ADD\_ARC\_UNIT(var\_name)](#macro_add_arc_unitvar_name)
    - [MACRO\_ADD\_ARC\_UNIT\_ALPHA(var\_name)](#macro_add_arc_unit_alphavar_name)
    - [MACRO\_ADD\_ARC\_HELMET(var\_scope,var\_name)](#macro_add_arc_helmetvar_scopevar_name)
    - [MACRO\_ADD\_ARC\_HELMET\_ILLUM(var\_scope,var\_name)](#macro_add_arc_helmet_illumvar_scopevar_name)
    - [MACRO\_ADD\_ARC\_HELMET\_ALPHA(var\_scope,var\_name)](#macro_add_arc_helmet_alphavar_scopevar_name)
    - [MACRO\_ADD\_ARC\_HELMET\_ALPHA\_ILLUM(var\_scope,var\_name)](#macro_add_arc_helmet_alpha_illumvar_scopevar_name)
    - [MACRO\_ADD\_ARC\_VEST(var\_scope,var\_name)](#macro_add_arc_vestvar_scopevar_name)
    - [MACRO\_ADD\_ARC\_VEST\_ALPHA(var\_scope,var\_name)](#macro_add_arc_vest_alphavar_scopevar_name)
    - [MACRO\_ADD\_ARC\_VEST\_ALPHA\_SHIELD(var\_scope,var\_name)](#macro_add_arc_vest_alpha_shieldvar_scopevar_name)
    - [MACRO\_ADD\_ARC\_UNIFORM(var\_scope,var\_name)](#macro_add_arc_uniformvar_scopevar_name)
    - [MACRO\_ADD\_ARC\_UNIFORM\_ALPHA(var\_scope,var\_name)](#macro_add_arc_uniform_alphavar_scopevar_name)
  - [Commando](#commando)
    - [MACRO\_ADD\_COMMANDO\_UNIT(var\_name,var\_number)](#macro_add_commando_unitvar_namevar_number)
    - [MACRO\_ADD\_COMMANDO\_UNIT\_SL(var\_name,var\_number)](#macro_add_commando_unit_slvar_namevar_number)
    - [MACRO\_ADD\_COMMANDO\_BACKPACK(var\_scope,var\_name,var\_number)](#macro_add_commando_backpackvar_scopevar_namevar_number)
    - [MACRO\_ADD\_COMMANDO\_SPEC\_BACKPACK(var\_scope,var\_name,var\_number,var\_spec)](#macro_add_commando_spec_backpackvar_scopevar_namevar_numbervar_spec)
    - [MACRO\_ADD\_COMMANDO\_TECH\_BACKPACK(var\_scope,var\_name,var\_number)](#macro_add_commando_tech_backpackvar_scopevar_namevar_number)
    - [MACRO\_ADD\_COMMANDO\_HELMET(var\_scope,var\_name,var\_number)](#macro_add_commando_helmetvar_scopevar_namevar_number)
    - [MACRO\_ADD\_COMMANDO\_UNIFORM(var\_scope,var\_name,var\_number)](#macro_add_commando_uniformvar_scopevar_namevar_number)
  - [Jumptroopers](#jumptroopers)
    - [MACRO\_ADD\_JT\_UNIT(var\_name)](#macro_add_jt_unitvar_name)
    - [MACRO\_ADD\_JT\_BACKPACK(var\_scope,var\_name)](#macro_add_jt_backpackvar_scopevar_name)
    - [MACRO\_ADD\_JT\_HELMET(var\_scope,var\_name)](#macro_add_jt_helmetvar_scopevar_name)
    - [MACRO\_ADD\_JT\_HELMET\_ILLUM(var\_scope,var\_name)](#macro_add_jt_helmet_illumvar_scopevar_name)
    - [MACRO\_ADD\_JT\_UNIFORM(var\_scope,var\_name)](#macro_add_jt_uniformvar_scopevar_name)
  - [Covert-Ops](#covert-ops)
    - [MACRO\_ADD\_ASSASSIN\_UNIT(var\_name)](#macro_add_assassin_unitvar_name)
    - [MACRO\_ADD\_ASSASSIN\_HELMET(var\_scope,var\_name)](#macro_add_assassin_helmetvar_scopevar_name)
    - [MACRO\_ADD\_ASSASSIN\_VEST(var\_scope,var\_name)](#macro_add_assassin_vestvar_scopevar_name)
    - [MACRO\_ADD\_ASSASSIN\_UNIFORM(var\_scope,var\_name)](#macro_add_assassin_uniformvar_scopevar_name)
    - [MACRO\_ADD\_SHADOW\_UNIT(var\_name)](#macro_add_shadow_unitvar_name)
    - [MACRO\_ADD\_SHADOW\_HELMET(var\_scope,var\_name)](#macro_add_shadow_helmetvar_scopevar_name)
    - [MACRO\_ADD\_SHADOW\_UNIFORM(var\_scope,var\_name)](#macro_add_shadow_uniformvar_scopevar_name)
  - [Field Support](#field-support)
    - [MACRO\_ADD\_FIELDSUPPORT\_UNIT(var\_name)](#macro_add_fieldsupport_unitvar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_BACKPACK(var\_scope,var\_name)](#macro_add_fieldsupport_backpackvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_SPECOPS(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_specopsvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_SPECOPS\_ILLUM(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_specops_illumvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_TANKER(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_tankervar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_TANK(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_tankvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_TANK\_ILLUM(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_tank_illumvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_PHASE1(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_phase1var_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_PHASE1\_ILLUM(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_phase1_illumvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_PHASE2(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_phase2var_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_PHASE2\_ILLUM(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_phase2_illumvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_ARF(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_arfvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_ARF\_ILLUM(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_arf_illumvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_AIRBORNE(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_airbornevar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_AIRBORNE\_ILLUM(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_airborne_illumvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_ENGINEER(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_engineervar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_HELMET\_ENGINEER\_ILLUM(var\_scope,var\_name)](#macro_add_fieldsupport_helmet_engineer_illumvar_scopevar_name)
    - [MACRO\_ADD\_FIELDSUPPORT\_UNIFORM(var\_scope,var\_name)](#macro_add_fieldsupport_uniformvar_scopevar_name)
  - [Pilot](#pilot)
    - [MACRO\_ADD\_PILOT\_UNIT(var\_name)](#macro_add_pilot_unitvar_name)
    - [MACRO\_ADD\_PILOT\_BACKPACK(var\_scope,var\_name)](#macro_add_pilot_backpackvar_scopevar_name)
    - [MACRO\_ADD\_PILOT\_HELMET\_P1(var\_scope,var\_name)](#macro_add_pilot_helmet_p1var_scopevar_name)
    - [MACRO\_ADD\_PILOT\_HELMET\_P1\_ILLUM(var\_scope,var\_name)](#macro_add_pilot_helmet_p1_illumvar_scopevar_name)
    - [MACRO\_ADD\_PILOT\_HELMET\_P2(var\_scope,var\_name)](#macro_add_pilot_helmet_p2var_scopevar_name)
    - [MACRO\_ADD\_PILOT\_HELMET\_P3(var\_scope,var\_name)](#macro_add_pilot_helmet_p3var_scopevar_name)
    - [MACRO\_ADD\_PILOT\_UNIFORM(var\_scope,var\_name)](#macro_add_pilot_uniformvar_scopevar_name)
  - [Trooper](#trooper)
    - [MACRO\_ADD\_TROOPER\_UNIT(var\_name)](#macro_add_trooper_unitvar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_SPECOPS(var\_scope,var\_name)](#macro_add_trooper_helmet_specopsvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_SPECOPS\_LR(var\_scope,var\_name)](#macro_add_trooper_helmet_specops_lrvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_SPECOPS\_ILLUM(var\_scope,var\_name)](#macro_add_trooper_helmet_specops_illumvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_SPECOPS\_LR\_ILLUM(var\_scope,var\_name)](#macro_add_trooper_helmet_specops_lr_illumvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_PHASE1(var\_scope,var\_name)](#macro_add_trooper_helmet_phase1var_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_PHASE1\_ILLUM(var\_scope,var\_name)](#macro_add_trooper_helmet_phase1_illumvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_PHASE2(var\_scope,var\_name)](#macro_add_trooper_helmet_phase2var_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_PHASE2\_ILLUM(var\_scope,var\_name)](#macro_add_trooper_helmet_phase2_illumvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_ARF(var\_scope,var\_name)](#macro_add_trooper_helmet_arfvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_ARF\_ILLUM(var\_scope,var\_name)](#macro_add_trooper_helmet_arf_illumvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_AIRBORNE(var\_scope,var\_name)](#macro_add_trooper_helmet_airbornevar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_AIRBORNE\_ILLUM(var\_scope,var\_name)](#macro_add_trooper_helmet_airborne_illumvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_ENGINEER(var\_scope,var\_name)](#macro_add_trooper_helmet_engineervar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_HELMET\_ENGINEER\_ILLUM(var\_scope,var\_name)](#macro_add_trooper_helmet_engineer_illumvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_VEST\_COMMAND(var\_scope,var\_name)](#macro_add_trooper_vest_commandvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_VEST\_COMMAND\_SHIELD(var\_scope,var\_name)](#macro_add_trooper_vest_command_shieldvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_VEST\_PLATOON(var\_scope,var\_name)](#macro_add_trooper_vest_platoonvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_CP\_VEST\_CUSTOM(var\_scope,var\_name)](#macro_add_trooper_cp_vest_customvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_CS\_VEST\_CUSTOM(var\_scope,var\_name)](#macro_add_trooper_cs_vest_customvar_scopevar_name)
    - [MACRO\_ADD\_TROOPER\_UNIFORM(var\_scope,var\_name)](#macro_add_trooper_uniformvar_scopevar_name)


# How 2 Add Textures

1. Place texture files in correct directory, ensure correct filename
    - Reference the file path pattern using the macro reference below
2. Add the appropriate macro to the relevant `.hpp` files
    - Don't forget the `;` at the end of the line
3. Done!
    - Use `hemtt check` (if installed) to verify your work

The steps below are **optional**, most of this is also handled by workflows or during the update release preparation:

4. Verify correct path names by running the paths checking script (requires Python 3 & hemtt)
    - Run `hemtt build`
    - Run `python .\tools\check_paths.py` (add `-h` behind the file name to show tool help)
5. Update ACEAX Compat by running the tool (requires Python 3 & hemtt)
    - Run `hemtt build`
    - Run `python .\tools\write_aceax_compat.py` (add `-h` behind the file name to show tool help)
6. Update ground holders by running the tool (requires Python 3, hemtt, Arma 3)
    - Run `hemtt launch`
    - When in-game, open the 3den editor and create a new mission file in VR (fastest loading time)
    - In the 3den Editor, open the Debug Console and enter the following line of code `["sob"] call mti_common_fnc_grabGroundHolderData;`
    - Press Enter and wait for the command to finish, after which you should have JSON-formatted data in your clipboard
    - Run `python .\tools\write_ground_holders.py`
7. Update `config_lists.hpp` files by running the tool (requires Python 3 & hemtt)
    - Run `hemtt build`
    - Run `python .\tools\write_config_lists.py` (add `-h` behind the file name to show tool help)

## Differences from v1 to v2

- Arsenal whitelist entries are now handled by the macro
- Compatibility bindings for ACE Extended Arsenal (`XtdGearModels.hpp` file) are now written automatically using a script
- `config_lists.hpp` files are now automatically updated via scripts
- Ground Holders are now created using a script

# Macro Reference

## Legend

- Substitute variables surrounded by `##` in file path names
- `var_name` must **not** contain spaces or special characters other than an underscore `_`

## ARC

### MACRO_ADD_ARC_UNIT(var_name)
- Description: ARC Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\uniforms\custom\##var_name##\clone_armor1_##var_name##_co.paa`
    - `data\uniforms\custom\##var_name##\clone_armor2_##var_name##_co.paa`

### MACRO_ADD_ARC_UNIT_ALPHA(var_name)
- Description: Alpha ARC Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\uniforms\custom\alpha_##var_name##\clone_armor1_alpha_##var_name##_co.paa`
    - `data\uniforms\custom\alpha_##var_name##\clone_armor2_alpha_##var_name##_co.paa`

### MACRO_ADD_ARC_HELMET(var_scope,var_name)
- Description: ARC Helmet
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\clone_helmet_arc_##var_name##_co.paa`

### MACRO_ADD_ARC_HELMET_ILLUM(var_scope,var_name)
- Description: ARC Helmet (Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\clone_helmet_arc_##var_name##_co.paa`

### MACRO_ADD_ARC_HELMET_ALPHA(var_scope,var_name)
- Description: Alpha ARC Helmet
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\P1_Helmet_Alpha_##var_name##_co.paa`

### MACRO_ADD_ARC_HELMET_ALPHA_ILLUM(var_scope,var_name)
- Description: Alpha ARC Helmet (Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\P1_Helmet_Alpha_##var_name##_co.paa`

### MACRO_ADD_ARC_VEST(var_scope,var_name)
- Description: ARC Vest
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\vests\custom\clone_vest_arc_##var_name##_co.paa`

### MACRO_ADD_ARC_VEST_ALPHA(var_scope,var_name)
- Description: Alpha ARC Vest
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\vests\custom\Clone_vest_alpha_##var_name##_co.paa`

### MACRO_ADD_ARC_VEST_ALPHA_SHIELD(var_scope,var_name)
- Description: Alpha ARC Vest (w/ Shield)
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\vests\custom\Clone_vest_alpha_##var_name##_co.paa`

### MACRO_ADD_ARC_UNIFORM(var_scope,var_name)
- Description: ARC Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A

### MACRO_ADD_ARC_UNIFORM_ALPHA(var_scope,var_name)
- Description: Alpha ARC Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A

## Commando

### MACRO_ADD_COMMANDO_UNIT(var_name,var_number)
- Description: RC Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
    - `var_number`: RC Number
- File Path Pattern:
    - `data\uniforms\Custom\##var_name##\camo1_##var_name##_co.paa`
    - `data\uniforms\Custom\##var_name##\camo2_##var_name##_co.paa`

### MACRO_ADD_COMMANDO_UNIT_SL(var_name,var_number)
- Description: RC Unit (Squad Leader)
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
    - `var_number`: RC Number
- File Path Pattern:
    - `data\uniforms\Custom\##var_name##\camo1_##var_name##_co.paa`
    - `data\uniforms\Custom\##var_name##\camo2_##var_name##_co.paa`

### MACRO_ADD_COMMANDO_BACKPACK(var_scope,var_name,var_number)
- Description: RC Backpack (Standard)
- Location: `cfg\backpacks.hpp`
- Arguments:
    - `var_scope`: Visibility (usuallly always `2`)
    - `var_name`: Class & Display Name
    - `var_number`: RC Number
- File Path Pattern: `data\Backpacks\Custom\backpack_##var_name##_co.paa`

### MACRO_ADD_COMMANDO_SPEC_BACKPACK(var_scope,var_name,var_number,var_spec)
- Description: RC Backpack (Spec)
- Location: `cfg\backpacks.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
    - `var_number`: RC Number
    - `var_spec`: Backpack subclass, one of `rto`, `eod`
- File Path Pattern: `data\Backpacks\Custom\backpack_##var_name##_co.paa`

### MACRO_ADD_COMMANDO_TECH_BACKPACK(var_scope,var_name,var_number)
- Description: RC Backpack (Tech)
- Location: `cfg\backpacks.hpp`
- Arguments:
    - `var_scope`: Visibility (usuallly always `2`)
    - `var_name`: Class & Display Name
    - `var_number`: RC Number
- File Path Pattern:
    - `data\Backpacks\Custom\backpack_##var_name##_co.paa`
    - `data\Backpacks\Custom\backpack_tech_##var_name##_co.paa`

### MACRO_ADD_COMMANDO_HELMET(var_scope,var_name,var_number)
- Description: RC Helmet
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usuallly always `2`)
    - `var_name`: Class & Display Name
    - `var_number`: RC Number
- File Path Pattern: `data\helmets\Custom\helmet_##var_name##_co.paa`

### MACRO_ADD_COMMANDO_UNIFORM(var_scope,var_name,var_number)
- Description: RC Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usuallly always `2`)
    - `var_name`: Class & Display Name
    - `var_number`: RC Number
- File Path Pattern: N/A

## Jumptroopers

### MACRO_ADD_JT_UNIT(var_name)
- Description: JT Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\uniforms\custom\##var_name##\clone_armor1_##var_name##_co.paa`
    - `data\uniforms\custom\##var_name##\clone_armor2_##var_name##_co.paa`

### MACRO_ADD_JT_BACKPACK(var_scope,var_name)
- Description: JT Jumppack
- Location: `cfg\backpacks.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Backpacks\custom\Clone_jumppack_##var_name##_JT12_co.paa`

### MACRO_ADD_JT_HELMET(var_scope,var_name)
- Description: JT Helmet
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\P1_Helmet_##var_name##_co.paa`

### MACRO_ADD_JT_HELMET_ILLUM(var_scope,var_name)
- Description: JT Helmet (Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\P1_Helmet_##var_name##_co.paa`

### MACRO_ADD_JT_UNIFORM(var_scope,var_name)
- Description: JT Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A

## Covert-Ops

### MACRO_ADD_ASSASSIN_UNIT(var_name)
- Description: Assassin Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\Uniforms\custom\##var_name##\clone_armor1_##var_name##_co.paa`
    - `data\Uniforms\custom\##var_name##\clone_armor2_##var_name##_co.paa`

### MACRO_ADD_ASSASSIN_HELMET(var_scope,var_name)
- Description: Assassin Helmet
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Helmets\clone_helmet_BARC_##var_name##_co.paa`

### MACRO_ADD_ASSASSIN_VEST(var_scope,var_name)
- Description: Assassin Vest
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\vests\Clone_vest_assassin_##var_name##_co.paa`

### MACRO_ADD_ASSASSIN_UNIFORM(var_scope,var_name)
- Description: Assassin Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A

### MACRO_ADD_SHADOW_UNIT(var_name)
- Description: Shadow Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\uniforms\custom\##var_name##\clone_armor1_##var_name##_co.paa`
    - `data\uniforms\custom\##var_name##\clone_armor2_##var_name##_co.paa`

### MACRO_ADD_SHADOW_HELMET(var_scope,var_name)
- Description: Shadow Helmet
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\Clone_helmet_P2_##var_name##_co.paa`

### MACRO_ADD_SHADOW_UNIFORM(var_scope,var_name)
- Description: Shadow Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A

## Field Support

### MACRO_ADD_FIELDSUPPORT_UNIT(var_name)
- Description: FS Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\uniforms\##var_name##\clone_armor1_##var_name##_co.paa`
    - `data\uniforms\##var_name##\clone_armor2_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_BACKPACK(var_scope,var_name)
- Description: FS Backpack
- Location: `cfg\backpacks.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\backpacks\fs-b\camo_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_SPECOPS(var_scope,var_name)
- Description: FS Helmet (Specops)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\SpecOpsHelmet_##var_name##_CO.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_SPECOPS_ILLUM(var_scope,var_name)
- Description: FS Helmet (Specops, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\SpecOpsHelmet_##var_name##_CO.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_TANKER(var_scope,var_name)
- Description: FS Helmet (Tanker)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Clone_helmet_tanker_##var_name##_CO.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_TANK(var_scope,var_name)
- Description: FS Helmet (Tank)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Clone_helmet_tanker_##var_name##_CO.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_TANK_ILLUM(var_scope,var_name)
- Description: FS Helmet (Tank, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Clone_helmet_tanker_##var_name##_CO.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_PHASE1(var_scope,var_name)
- Description: FS Helmet (Phase1)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Phase1_helmet_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_PHASE1_ILLUM(var_scope,var_name)
- Description: FS Helmet (Phase1, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Phase1_helmet_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_PHASE2(var_scope,var_name)
- Description: FS Helmet (Phase2)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\clone_helmet_P2_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_PHASE2_ILLUM(var_scope,var_name)
- Description: FS Helmet (Phase2, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\clone_helmet_P2_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_ARF(var_scope,var_name)
- Description: FS Helmet (Arf)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_ARF_##var_name##_co.paa)`

### MACRO_ADD_FIELDSUPPORT_HELMET_ARF_ILLUM(var_scope,var_name)
- Description: FS Helmet (Arf, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_ARF_##var_name##_co.paa)`

### MACRO_ADD_FIELDSUPPORT_HELMET_AIRBORNE(var_scope,var_name)
- Description: FS Helmet (Airborne)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Clone_helmet_AB_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_AIRBORNE_ILLUM(var_scope,var_name)
- Description: FS Helmet (Airborne, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Clone_helmet_AB_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_ENGINEER(var_scope,var_name)
- Description: FS Helmet (Engineer)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_Engineer_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_HELMET_ENGINEER_ILLUM(var_scope,var_name)
- Description: FS Helmet (Engineer, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_Engineer_##var_name##_co.paa`

### MACRO_ADD_FIELDSUPPORT_UNIFORM(var_scope,var_name)
- Description: FS Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A

## Pilot

### MACRO_ADD_PILOT_UNIT(var_name)
- Description: Pilot Unit
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\uniforms\custom\##var_name##\clone_armor1_##var_name##_co.paa`
    - `data\uniforms\custom\##var_name##\clone_armor2_##var_name##_co.paa`

### MACRO_ADD_PILOT_BACKPACK(var_scope,var_name)
- Description: Pilot Survival Pack
- Location: `cfg\backpacks.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Backpacks\Clone_jumppack_##var_name##_co.paa`

### MACRO_ADD_PILOT_HELMET_P1(var_scope,var_name)
- Description: Pilot Helmet (P1)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\Helmets\P1_Customs\##var_name##\PilotHelmet_##var_name##_co.paa`
    - `data\Helmets\P1_Customs\##var_name##\LifeSupport_##var_name##_co.paa`

### MACRO_ADD_PILOT_HELMET_P1_ILLUM(var_scope,var_name)
- Description: Pilot Helmet (P1, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\Helmets\P1_Customs\##var_name##\PilotHelmet_##var_name##_co.paa`
    - `data\Helmets\P1_Customs\##var_name##\LifeSupport_##var_name##_co.paa`

### MACRO_ADD_PILOT_HELMET_P2(var_scope,var_name)
- Description: Pilot Helmet (P2)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Helmets\P2_Customs\Phase2_Pilot_##var_name##_co.paa`

### MACRO_ADD_PILOT_HELMET_P3(var_scope,var_name)
- Description: Pilot Helmet (P3)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Helmets\P3_Customs\Phase3_Pilot_Helmet_##var_name##_co.paa`

### MACRO_ADD_PILOT_UNIFORM(var_scope,var_name)
- Description: Pilot Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A

## Trooper

### MACRO_ADD_TROOPER_UNIT(var_name)
- Description: Trooper Uniform
- Location: `cfg\units.hpp`
- Arguments:
    - `var_name`: Class & Display Name
- File Path Pattern:
    - `data\uniforms\custom\##var_name##\clone_armor1_##var_name##_co.paa`
    - `data\uniforms\custom\##var_name##\clone_armor2_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_SPECOPS(var_scope,var_name)
- Description: Trooper Helmet (Specops)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\SpecOpsHelmet_##var_name##_CO.paa`

### MACRO_ADD_TROOPER_HELMET_SPECOPS_LR(var_scope,var_name)
- Description: Trooper Helmet (Specops, Antenna)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\SpecOpsHelmet_##var_name##_CO.paa`

### MACRO_ADD_TROOPER_HELMET_SPECOPS_ILLUM(var_scope,var_name)
- Description: Trooper Helmet (Specops, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\SpecOpsHelmet_##var_name##_CO.paa`

### MACRO_ADD_TROOPER_HELMET_SPECOPS_LR_ILLUM(var_scope,var_name)
- Description: Trooper Helmet (Specops, Antenna, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\SpecOpsHelmet_##var_name##_CO.paa`

### MACRO_ADD_TROOPER_HELMET_PHASE1(var_scope,var_name)
- Description: Trooper Helmet (Phase1)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Phase1_helmet_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_PHASE1_ILLUM(var_scope,var_name)
- Description: Trooper Helmet (Phase1, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Phase1_helmet_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_PHASE2(var_scope,var_name)
- Description: Trooper Helmet (Phase2)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\clone_helmet_P2_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_PHASE2_ILLUM(var_scope,var_name)
- Description: Trooper Helmet (Phase2, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\clone_helmet_P2_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_ARF(var_scope,var_name)
- Description: Trooper Helmet (Arf)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_ARF_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_ARF_ILLUM(var_scope,var_name)
- Description: Trooper Helmet (Arf, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_ARF_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_AIRBORNE(var_scope,var_name)
- Description: Trooper Helmet (Airborne)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Clone_helmet_AB_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_AIRBORNE_ILLUM(var_scope,var_name)
- Description: Trooper Helmet (Airborne, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Clone_helmet_AB_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_ENGINEER(var_scope,var_name)
- Description: Trooper Helmet (Engineer)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_Engineer_##var_name##_co.paa`

### MACRO_ADD_TROOPER_HELMET_ENGINEER_ILLUM(var_scope,var_name)
- Description: Trooper Helmet (Engineer, Blue Visor)
- Location: `cfg\helmets.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\helmets\custom\Helmet_Engineer_##var_name##_co.paa`

### MACRO_ADD_TROOPER_VEST_COMMAND(var_scope,var_name)
- Description: Trooper Command Vest
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Vests\Clone_vest_officer_##var_name##_co.paa`

### MACRO_ADD_TROOPER_VEST_COMMAND_SHIELD(var_scope,var_name)
- Description: Trooper Command Vest (Shield)
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Vests\Clone_vest_officer_##var_name##_co.paa`

### MACRO_ADD_TROOPER_VEST_PLATOON(var_scope,var_name)
- Description: Trooper Plt Command Vest
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Vests\Clone_vest_officer_##var_name##_co.paa`

### MACRO_ADD_TROOPER_CP_VEST_CUSTOM(var_scope,var_name)
- Description: Trooper CP Kama
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Vests\Clone_vest_Corporal_##var_name##_co.paa`

### MACRO_ADD_TROOPER_CS_VEST_CUSTOM(var_scope,var_name)
- Description: Trooper CS Vest
- Location: `cfg\vests.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: `data\Vests\Clone_vest_officer_##var_name##_co.paa`

### MACRO_ADD_TROOPER_UNIFORM(var_scope,var_name)
- Description: Trooper Uniform
- Location: `cfg\uniforms.hpp`
- Arguments:
    - `var_scope`: Visibility (usually always `2`)
    - `var_name`: Class & Display Name
- File Path Pattern: N/A
