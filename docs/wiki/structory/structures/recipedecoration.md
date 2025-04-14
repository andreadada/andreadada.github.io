---
layout: default
title: RecipeDecoration
parent: Structory
grand_parent: Wiki
back_to_top: true
back_to_top_text: "Back to top"
---



A recipe decoration is a container of some decorations that other features might use

You can tell how to decorate some events (for example: when using the crafting)

For now it supports particle and sound only

example:
```yaml
xyzdecoration:
    particle:
      type: FLAME
      particle: SOUL_FIRE_FLAME
      amount: 10
      count: 1
      center-offset: "0 0 0"
      speed: 0
    sound:
      type: ENTITY_BLAZE_SHOOT
      volume: 1
      pitch: 0
```


