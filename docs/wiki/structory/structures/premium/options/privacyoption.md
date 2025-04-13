---
layout: default
title: PrivacyOption 🔒
parent: Options
grand_parent: Structory
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 3.1
---


Let your structure only yours


| Key  |  Type  |                                   Description                                   |
|:-----|:------:|:-------------------------------------------------------------------------------:|
| type | Policy | This is the policy that the structure will use to protect itself from strangers |


Each single Policy has its attributes, so you have to see each single Policy to properly configure the structure.

At the moment the only Policy implemented is "owneronly" which lets the structure's creator access the structure


example:
```yaml
structure:
  name: "...."
  #others stuff
  options:
    privacy:
      type: owneronly
```
