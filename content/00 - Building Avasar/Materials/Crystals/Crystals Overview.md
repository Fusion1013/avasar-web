---
tags:
- material_overview
editors: Fusion
---
## Overview
This documents contain a variety of different crystals, which is a type of [[Materials Overview|Material]].
## List of Crystals
```dataview
TABLE WITHOUT ID
file.link AS "Material",
description AS "Description",
properties AS "Properties",
rarity AS "Rarity"
FROM #material AND #crystal
WHERE description != null
SORT file.link ASC
```
