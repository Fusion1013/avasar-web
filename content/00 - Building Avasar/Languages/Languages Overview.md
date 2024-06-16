---
aliases:
- Language
- Languages
- Language Group
---
## Languages & Groups
```dataview
TABLE WITHOUT ID
file.link AS "Language/Group",
choice(language_group = null, "**Group**", "Language") AS "Type",
regions AS "Regions",
default(language_group, file.name) AS "Group"
FROM (#language AND -#Dead) OR #Language_Group
SORT (default(language_group, file.name)+choice(language_group = null, "Group", "Language")) ASC
```
## Languages Grouped by Type
```dataviewjs
for (let group of dv.pages("#language").where(p => p.language_group != null).groupBy(p => p.language_group)) {
	dv.header(3, group.key);
	dv.table(["Name", "Regions"],
		group.rows
			.sort(k => k['Plain Rating'], 'desc')
			.map(k => [k.file.link, k.regions]))
}
```

![[Language Map.canvas|Language Map]]
