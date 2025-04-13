---
layout: default
title: BlockDisplayOption 🔒
parent: Options
grand_parent: Structory
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 3.2
---

With this Option you can display custom block display when a structure is created.



| Key       |     Type     |                         Description                         |
|:----------|:------------:|:-----------------------------------------------------------:|
| key       | BlockDisplay |          This is the block display that will spawn          |
| direction |  Direction   | The direction that the Block Display will face when spawned |

example:
```yaml
structure:
  name: "...."
  #others stuff
  options:
    blockdisplay:
      key: generator_1
      direction: DIRECT
```
