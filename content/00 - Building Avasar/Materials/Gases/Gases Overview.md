---
tags:
- material_overview
---
## Overview
This documents contain a variety of different gases, which is a type of [[Materials Overview|Material]].
## List of Gases
```dataview
TABLE WITHOUT ID
file.link AS "Material",
description AS "Description",
properties AS "Properties",
rarity AS "Rarity"
FROM #material AND #gas
WHERE description != null
SORT file.link ASC
```
