# Fortify (MokTech Edition)
## Introduction

This system is based on **ACE3's Fortify Framework** (formerly from ACEX), originally created by Kingsley. We have introduced some new elements and changes to it, to make it more modular and to make it fit in more nicely with our plans for Logistics and Field Support.

In short, those differences can be summed up as follows:

* Available Fortifications are determined by nearby "**containers**"
* Those same containers also determine the **available budget** (instead of a global budget)
* Deployed objects can be quickly recalled to containers for ease of transport
* Certain containers additionally allow **saving nearby deployed objects** into a "composition", to be loaded at a later point
* Other containers can deploy certain **prefab compositions** (eg. Field LZ, Forward Observation Posts, etc)
* Access to the Fortify System is enabled by a **special backpack** (instead of an arbitrary inventory item)

More detailed information on the above can be found in the succeeding sections.

## Table of Contents
- [Fortify (MokTech Edition)](#fortify-moktech-edition)
  - [Introduction](#introduction)
  - [Table of Contents](#table-of-contents)
  - [Presets](#presets)
    - [Budgets & Limits](#budgets--limits)
    - [Recalling Objects](#recalling-objects)
  - [Save/Load Containers](#saveload-containers)
    - [Managing Saved Compositions](#managing-saved-compositions)
  - [Compositions](#compositions)

**For developers and mission makers**, please visit the following page for information on how to define your own presets/compositions and containers (and some other neat tricks):

* [dev.md](dev.md)

## Presets

A preset defines a set of objects and their associated costs which can be deployed using Fortify. There are fundamentally two types of presets: Backpack-bound and Container-bound. The former only require a compatible backpack in order to be able to deploy objects; the latter requires a compatible container in the player's vicinity (in addition to the backpack).

### Budgets & Limits

Every container (and the backpack) has an internal budget for each preset, which gets depleted as objects are deployed from them. Additionally, a preset can also set a hard limit on certain objects (eg. a Portable Shield Generator can only ever be deployed once from the backpack).

### Recalling Objects

Since the Fortify backpack and the containers have a local budget, we have added an option to quickly recall all objects that were deployed from that container (or the backpack). This is especially useful if the container is to be moved to new location, and you do not want to leave useless junk behind.

Backpack Objects can be recalled using the corresponding ACE Self-Interaction. Container Objects can be recalled by interacting with the container directly.

## Save/Load Containers

The Save/Load container is a special type of container which allows players to save their builds into a composition and to later load it again. This save is persistent (stored in the player's profile variables), so builds can be saved and re-used across several missions, for example.

**Only objects that were previously deployed** either directly through Fortify or by a composition will be included in the save.

By default, the range in which objects are saved is ~150 metres.

### Managing Saved Compositions

Compositions saved through the save/load container can be managed by using the corresponding ACE Self-Interaction.

## Compositions

Compositions are pre-defined structures that can be deployed from special containers in the field. To deploy a composition, interact directly with the container it belongs to and choose "deploy". The preview allows precise positioning of the prefab before placing it.

Similary to Fortify itself, composition containers also have an internal **budget**. Previously deployed compositions can also be recalled again by interacting with the container.
