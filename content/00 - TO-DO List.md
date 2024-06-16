# TO-DO Notes
```dataview
TABLE
todo AS "Message",
choice(editors = null, "Unassigned", editors) AS Editors
WHERE todo != null
SORT (choice(editors = null, "z", editors) + file.name) ASC
```
