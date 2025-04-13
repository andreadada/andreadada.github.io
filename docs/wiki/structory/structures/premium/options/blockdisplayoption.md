---
layout: default
title: BlockDisplayOption 🔒
parent: Options
grand_parent: Premium
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 4.1
---

With this Option you can display custom block display when a structure is created.



| Key       |                                            Type                                            |                         Description                         |
|:----------|:------------------------------------------------------------------------------------------:|:-----------------------------------------------------------:|
| key       | [BlockDisplay]({{site.baseurl}}/docs/wiki/structory/structures/premium/blockdisplay.html). |          This is the block display that will spawn          |
| direction |    [Direction]({{site.baseurl}}/docs/wiki/structory/structures/premium/direction.html).    | The direction that the Block Display will face when spawned |

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
