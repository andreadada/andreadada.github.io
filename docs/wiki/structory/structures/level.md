---
layout: default
title: Level
parent: Structory
grand_parent: Wiki
back_to_top: true
back_to_top_text: "Back to top"
---


A level represent a section of a structure's block scheme. It has a fixed Y that tells how 
far is the level from the center of the structure along the Y axis.

## Level

| Parameter | Type            | Required | Value                         |
|:----------|-----------------|----------|:------------------------------|
| level     | Integer         | true     | Number, positive and negative |
| type      | String          | true     | "Standard" i will remove this |
| checkers  | Set of Checkers | false    | Vector offset                 |

## Checker

A checker define the layout, blocks locations and material to compare.


| Parameter | Type                | Required | Value                              |
|:----------|---------------------|----------|:-----------------------------------|
| types     | Set of Placeholders | true     | Assign a block type to a character |
| main      | List of String      | true     | Create the layout of that level    |

> types must be defined as ```yaml X: Material``` with X that can be any character
> each single row defined in main must contain equal number of columns of others row

<details open markdown="block">
<summary>
    Example of checkers
</summary>
```yaml
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
```
</details>



Example of a level
```yaml
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
```