---
layout: default
title: Recipe
parent: Crafting
grand_parent: Structory
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 5.1
---


A recipe is a composition of Ingredients and Results, 

### PREMIUM
In the premium version, a Recipe can be part of groups. By default, if nothing is specified, it is added in the DEFAULT RecipeGroup.
A RecipeGroup is automatically created when you specify a new recipe-group in a Recipe's config file.


### Config Structure

You can define a new recipe in a .yml file inside ../plugins/Structory/recipes/ folder.

You can define different recipes in a single file. Each single node will be translated to a new Recipe.

| Parameter    | Type                 | Description                                         | Optional |
|:-------------|:---------------------|:----------------------------------------------------|:---------|
| recipe-group | Set of Strings       | It is PREMIUM only, by default it is DEFAULT.       | true     |
| ingredients  | Nodes of Ingredients | Each single node will be translated to a Ingredient | false    |
| results      | Nodes of Results     | Each single node will be translated to a Result     | false    |



### Config Structure
From 1.1.0 there are some special ingredients that can act as an index, they are used to increase efficiency in finding  
the correct Recipe when crafting.
You should always add a indexed Ingredient to a Recipe, for example: 'material' condition of the ItemIngredient is indexed.


### Ingredients

At the moment there are only 3 ingredients:

ItemIngredient, CustomItemIngredient and ExperienceIngredient (Premium Only)


### Example
```yaml
strange_apple:
  name: strange_apple
  group: "GOD_APPLE" #this can be a set of Strings ->  ["DEFAULT","GROUP1"...]
  ingredients:
    one:
      type: item
      material: APPLE
    two:
      type: item
      material: NETHER_WART
  result:
    one:
      type: saveditem
      offset: "0 0 0"
      key: strangeapple
```
