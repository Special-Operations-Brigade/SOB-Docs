# MUTT-L
===================

- [MUTT-L](#mutt-l)
  - [General Features](#general-features)
  - [Plow Features](#plow-features)
    - [Vertical Adjustments](#vertical-adjustments)
    - [Horizontal Adjustments](#horizontal-adjustments)
    - [Work Mode](#work-mode)
      - [Trench Digging](#trench-digging)


The MUTT-L is the specialized logistics variant of the MUTT framework, aimed at providing battlefield support in a variety of roles.

## General Features
- 4 passenger seats (in addition to the standard 3 crew seats)
- Similar ACE cargo space as the MUTT-C
- RRR through the ACE3 vehicle servicing framework
- Access to mti_aircraft servicing framework for the sake of convenience
- Built-in fortify presets: small/medium fortifications, h-barriers

## Plow Features

### Vertical Adjustments

The plow has three possible vertical positions:

- **Raised**: No speed limit, plow fully raised for traversing uneven terrain at high speed
- **Levelled**: No speed limit, default setting
- **Lowered**: 12km/h speed limit, work mode

### Horizontal Adjustments

The left and right shovel can be freely adjusted independently. These adjustments are purely visual.

### Work Mode

When the plow is lowered (see above) it is considered to be in "work mode". While in work mode, the speed of the MUTT-L is limited to 12 km/h.
The following effects take place without requiring further action while in work mode:

- Mines in the area in front of the plow are "safely" and reliably detonated
- Trenches and craters in front of the plow are levelled
- Vehicle wrecks and certain physX objects are attached to the front of the plow to allow moving them out of the way

#### Trench Digging

While in work mode, the plow can be set to dig trenches. While trench digging is enabled, the other work mode functions above *do not work*.
Driving forward with trench digging enabled will begin creating a trench of the selected type if the surface under the plow permits trench building.
While driving forward, the trench will slowly be built up to its max height and stay attached to the plow until the vehicle is stopped and reversed or the plow is raised.
