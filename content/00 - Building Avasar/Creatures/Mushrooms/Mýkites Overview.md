# Mýkites Overview
## Introduction
A Mýkite refers to any sort of living mushroom-type entity.
## List of Mýkites
```dataview
TABLE
creature_type AS Type,
environment AS Environment,
image AS Image
FROM #creature
WHERE creature_type = "Mýkite"
SORT creature_type ASC
```
