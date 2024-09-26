---
layout: default
title: Structory
parent: Structory
grand_parent: Wiki
---

Structures file must be placed in ./Structory/structures/
In a single file you can define more structures.

Structures must have a key and a name. No need to worry about the key since it is used the main node where you define a new structure.


| Parameter   | Type     | Required | Default |
|:------------|:---------|:---------|:-------:|
| name        | String   | true     |    *    |
| check-block | Material | false    |  null   |
| orientation | Boolean  | false    |  false  |
| options     | Options  | false    |  empty  |
| layout      | Layout   | false    |  empty  |

As you can see, only the name parameter is mandatory


| Parameter   | Description                                                                                                          |
|:------------|:---------------------------------------------------------------------------------------------------------------------|
| name        | Structure's display name                                                                                             |
| check-block | Block to check to activate the structure                                                                             |
| orientation | If the structure is symmetric or not, if true, there will be a check along each direction (NORTH, SOUTH, EAST, WEST) |
| options     | Options values, check [Options]({{site.baseurl}}/wiki/structory/options).                                            |
| layout      | Layout values, check [Layout]({{site.baseurl}}/wiki/structory/layout).                                               |



Example of a structure.
```yaml
elder_altar:
  name: "Elder Altar"
  check-block: CAULDRON
  orientation: false #check only EAST orientation, perfect if the structure is symmetric
  options:
    notify:
      message: "<white>You have created <light_purple>%structure%"
      actionbar: "<white>Now you can craft <light_purple>serious<white> items"
    crafting:
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
    particle:
      type: BOXSIZED
      amount: 15
      particle: PORTAL
      count: 1
      speed: 0.5
      center-offset: "0 1 0"
      start-point-offset: "-2.5 -0.6 -2.5"
      end-point-offset: "2.5 0.5 2.5"
    fireworks:
      type: RANDOM
      amount: 5
      power: 5
      flicker: true
      fade: PURPLE, BLACK, SILVER
      colors: FUCHSIA, PURPLE, WHITE, BLACK
  layout:
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
    levels:
      level0:
        level: 0
        type: STANDARD
        checkers:
          types:
            X: BLACKSTONE_WALL
            C: CAULDRON
          main:
            - "***X***"
            - "*X***X*"
            - "*******"
            - "X**C**X"
            - "*******"
            - "*X***X*"
            - "***X***"
      level-1:
        level: -1
        type: STANDARD
        checkers:
          types:
            C: CRYING_OBSIDIAN
            E: END_STONE
            O: OBSIDIAN
          main:
            - "***C***"
            - "*CEEEC*"
            - "*EOEOE*"
            - "CEECEEC"
            - "*EOEOE*"
            - "*CEEEC*"
            - "***C***"
```