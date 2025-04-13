---
layout: default
title: RebuildOption 🔒
parent: Options
grand_parent: Structory
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 3.1
---



Place blocks when the structure is deleted


| Key   |  Type  |                    Description                     |
|:------|:------:|:--------------------------------------------------:|
| build | Layout | Here you will add every layer like StructureLayout | |



example:
```yaml
structure:
  name: "...."
  #others stuff
  options:
    rebuild:
      build:
        center:
          order: 0
          offset: "0 0 0"
          type: place
          material: COPPER_BLOCK
        up:
          order: 1
          offset: "0 1 0"
          type: place
          material: COBBLED_DEEPSLATE_SLAB
```
