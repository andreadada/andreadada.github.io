---
layout: default
title: Layout
parent: Structory
grand_parent: Wiki
---


Layouts are part of a Structure. They are needed to set a structure's block scheme.

A Layout is composed of recipe-slots, levels and build sections.



| Parameter    | Type                                                                                       | Description                                                                    | Required | Default |
|:-------------|:-------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|:---------|:-------:|
| recipe-slots | [RecipeSlotLayout]({{site.baseurl}}/docs/wiki/structory/structures/recipeslotlayout.html). | Define recipe slots of the structure, if you want to make a crafting structure | false    |  empty  |
| levels       | Set of [Levels]({{site.baseurl}}/docs/wiki/structory/structures/level.html).               | A level is a scheme block with fixed Y offset from structure center.           | false    |  empty  |
| build        | Set of [Builders]({{site.baseurl}}/docs/wiki/structory/structures/builder.html).           | The name says it all, place or destroy blocks when a structure is activated    | false    |  empty  |



Example of a layout:
```yaml
layout:
  center-offset: "0 0 0"
  build:
    block0:
      type: DESTROY
      offset: "0 0 0"
    block1:
      offset: "0 1 0"
      type: PLACE
      material: PLAYER_HEAD
      texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvZGQzZWNlNTdmODYyZmUxNGIxZmVkY2Y4Zjc5NmNmMzE3NGU5MGNhY2ZiMDIwYTIxYjU5OWY4NDE2N2E2NjVkNyJ9fX0="
  levels:
    level0:
      level: 0
      type: STANDARD
      checkers:
        types:
          B: BEACON
          W: BLACKSTONE_WALL
        main:
          - "*W*W*"
          - "W***W"
          - "**B**"
          - "W***W"
          - "*W*W*"
    level-1:
      level: -1
      type: STANDARD
      checkers:
        types:
          O: OBSIDIAN
          C: CRYING_OBSIDIAN
          E: END_STONE
        main:
          - "OCOCO"
          - "CEEEC"
          - "OEEEO"
          - "CEEEC"
          - "OCOCO"
```