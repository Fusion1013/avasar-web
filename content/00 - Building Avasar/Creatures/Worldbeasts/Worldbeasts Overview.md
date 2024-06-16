---
banner: "![[PolyphemusGasGiant.jpg]]"
---
## Overview
Worldbeasts are giant beasts, forever cursed to wander their designated plane. One, and only one, exists on each plane.
## Beasts
```dataview
TABLE
plane AS "Plane",
image AS Image
FROM #worldbeast 
WHERE plane != "PLANE"
```
