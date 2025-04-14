---
layout: default
title: CraftingOption
parent: Options
grand_parent: Structory
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 3.1
---

If you want the structure to be able to craft, you have to add this Option.

Different from older version, now, the recipe slot layout must be set in this section.




| Parameter    | Type                                                                                       | Description                                                                    | Optional |
|:-------------|:-------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|:---------|
| recipe-slots | [RecipeSlotLayout]({{site.baseurl}}/docs/wiki/structory/structures/recipeslotlayout.html). | Define recipe slots of the structure, if you want to make a crafting structure | false    |
| insert       | RecipeDecoration                                                                           | When you insert an item in the structure.                                      | true     |
| place        | RecipeDecoration                                                                           | When you place (right click on a recipe slot) an item in the structure.        | true     |
| take         | RecipeDecoration                                                                           | When you take (right click on a recipe slot) an item from the structure.       | true     |
| consume      | RecipeDecoration                                                                           | When an ingredient is consumed while crafting                                  | true     |
| result       | RecipeDecoration                                                                           | When the item is prepared                                                      | true     |



example:
```yaml
structure:
  name: "...."
  #others stuff
  options:
    crafting:
      recipe-slots:
      offsets: #slots are ordered from up (first) to bottom (last)
        - "-3 0.0 0"
        - "-2 0.0 2"
        - "-2 0.0 -2"
        - "2 0.0 -2"
        - "2 0.0 2"
        - "0 0.0 3"
        - "0.0 0.0 -3"
        - "3 0.0 0.0"
      insert:
        sound:
          type: BLOCK_BREWING_STAND_BREW
          volume: 10
          pitch: 1
      place:
        sound:
          type: ENTITY_ITEM_FRAME_PLACE
          volume: 10
          pitch: 3
      take:
        sound:
          type: ENTITY_ITEM_FRAME_REMOVE_ITEM
          volume: 10
          pitch: 3
      consume:
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
      result:
        particle:
          type: FLAME
          particle: SOUL_FIRE_FLAME
          amount: 10
          count: 1
          center-offset: "0.0 0.5 0.0"
          speed: 0.1
        sound:
          type: ENTITY_DRAGON_FIREBALL_EXPLODE
          volume: 10
          pitch: 85
```
