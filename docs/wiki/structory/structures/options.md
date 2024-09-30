---
layout: default
title: Options
parent: Structory
grand_parent: Wiki
has_children: true
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 3
---


Options are objects that implements features to a structure.

They are defined in the options section in a structure section.


| Option         | Key      |  Type   |
|:---------------|----------|:-------:|
| CraftingOption | crafting |  FREE   |
| FireworkOption | firework |  FREE   |
| NotifyOption   | notify   |  FREE   |
| ParticleOption | particle |  FREE   |
| CommandOption  | command  | PREMIUM |
| DataOption     | data     | PREMIUM |


example:
```yaml
structurekey:
  name: "...."
  #others stuff
  options:
    optionkeyone:
      #stuff
    optionkeytwo:
      #stuff
```