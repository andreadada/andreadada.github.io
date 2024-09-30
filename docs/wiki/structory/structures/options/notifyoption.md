---
layout: default
title: NotifyOption
parent: Options
grand_parent: Structory
back_to_top: true
back_to_top_text: "Back to top"
nav_order: 3.1
---



Send custom message when a new instance is created


| Key       |     Type      |            Description             |
|:----------|:-------------:|:----------------------------------:|
| message   |    String     | Send this message to player's chat |
| title     |    String     |     Send this title to player      |
| subtitle  |    String     |    Send this subtitle to player    |
| actionbar |    String     |   Send this actionbar to player    |
| duration  |    Integer    |          Title's duration          |
| fade_in   |    Integer    |          Title's fade in           |
| fade_ou   |    Integer    |          Title's fade out          |



example:
```yaml
structurekey:
  name: "...."
  #others stuff
  options:
    notify:
      message: "<gray>You've created X structure !"
```
