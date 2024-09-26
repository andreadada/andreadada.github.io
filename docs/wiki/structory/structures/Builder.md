---
layout: default
title: Builder
parent: Structory
grand_parent: Wiki
back_to_top: true
back_to_top_text: "Back to top"
---

1. PlaceBuilder
2. HeadBuilder
3. DestroyBuilder
{:toc}

A builder is an entity that place/destroy blocks when a structure is created.

A generic builder is defined as follows:

```yaml
type: <BUILDERTYPE>
#others params
```

material parameter must be a valid value accepted by Spigot's Material
offset must be formatted as "X X X"  or "X.X X.YY X.ZZZ" X, Y and Z must be numbers


## PlaceBuilder


| Parameter | Type   | Required | Value              |
|:----------|--------|----------|:-------------------|
| type      | String | true     | "place"            |
| material  | String | true     | Spigot's Material  |
| offset    | String | false    | Vector offset      |

<details open markdown="block">
<summary>
    Example
</summary>
```yaml
block0:
    type: place
    material: STONE
```
</details>

* * *

## HeadBuilder

Special case of PlaceBuilder

| Parameter | Type   | Required | Value          |
|:----------|--------|----------|:---------------|
| type      | String | true     | "place"        |
| material  | String | true     | "PLAYER_HEAD"  |
| offset    | String | false    | Vector offset  |
| texture   | String | true     | Texture String |

<details open markdown="block">
<summary>
    Example
</summary>
```yaml
block0:
    type: place
    material: PLAYER_HEAD
    texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvZGQzZWNlNTdmODYyZmUxNGIxZmVkY2Y4Zjc5NmNmMzE3NGU5MGNhY2ZiMDIwYTIxYjU5OWY4NDE2N2E2NjVkNyJ9fX0="
```
</details>

* * *

## DestroyBuilder

| Parameter | Type   | Required | Value          |
|:----------|--------|----------|:---------------|
| type      | String | true     | "destroy"      |
| offset    | String | false    | Vector offset  |

<details open markdown="block">
<summary>
    Example
</summary>
```yaml
block0:
    type: destroy
    offset: "0 0 0"
```
</details>

* * *