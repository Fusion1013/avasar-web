# Creatures Overview
## List of Creatures
```dataview
TABLE
creature_type AS Type,
environment AS Environment,
image AS Image
FROM #creature
WHERE creature_type != "TEMPLATE"
SORT creature_type + file.name ASC
```
## Creatures by Environment
### Forest
```dataview
TABLE
creature_type AS Type,
image AS Image
FROM #creature
WHERE contains(join(environment, ""), "Caves")
```
### Caves
```dataview
TABLE
creature_type AS Type,
image AS Image
FROM #creature
WHERE contains(join(environment, ""), "Forest")
```
### Ocean
```dataview
TABLE
creature_type AS Type,
image AS Image
FROM #creature
WHERE contains(join(environment, ""), "Ocean")
```
