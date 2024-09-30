---
layout: default
title: CommandOption 🔒
parent: Options
grand_parent: Structory
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 3.2
---


PREMIUM
{: .label .label-yellow }


Automatically execute commands console-side when a new instance is created



| Key       |      Type      |            Description             |
|:----------|:--------------:|:----------------------------------:|
| commands  | List of String | Send this message to player's chat |



{: .note }
> PlaceholderAPI support is not implemented yet


Built-In placeholders - %key% = result



| Key          |      Result      |
|:-------------|:----------------:|
| player       |  player's name   |
| playeruuid   |  player's uuid   |
| structure    | structure's name |
| instanceuuid | instance's uuid  |

example:
```yaml
structurekey:
  name: "...."
  #others stuff
  options:
    command:
      commands:
        - "kill %player%"
        - "kick %player%"
```