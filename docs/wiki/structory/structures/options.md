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



| Option         | Key      | Type                             | Description |
|:---------------|----------|----------------------------------|:-----------:|
| CraftingOption | crafting | true                             |    TODO     |
| FireworkOption | firework | true                             |    TODO     |
| NotifyOption   | notify   | false                            |    TODO     |
| ParticleOption | particle | false                            |    TODO     |
| CommandOption  | command  | PREMIUM{: .label .label-yellow } |    TODO     |
| DataOption     | data     | PREMIUM{: .label .label-yellow } |    TODO     |


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