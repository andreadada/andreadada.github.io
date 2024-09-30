---
layout: default
title: RecipeSlotLayout
parent: Structory
grand_parent: Wiki
back_to_top: true
back_to_top_text: "Back to top"
---


Define where items will be displayed when inserting items to the structure.

| Parameter | Type            | Required | Value                             |
|:----------|-----------------|----------|:----------------------------------|
| offsets   | List of Strings | true     | Each line represent a recipe slot |



> At the moment you have to define each single offset by yourself, there is no scheme layout like levels.
> slots are ordered from up (first) to bottom (last)

Example
```yaml
recipe-slots:
  offsets: 
    - "-3 0.0 0"
    - "-2 0.0 2"
    - "-2 0.0 -2"
    - "2 0.0 -2"
    - "2 0.0 2"
    - "0 0.0 3"
    - "0.0 0.0 -3"
    - "3 0.0 0.0"
```