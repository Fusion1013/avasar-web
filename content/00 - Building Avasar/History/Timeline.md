## Overview
Certain types of events are marked by different icons.
**Empty Flag**: City Founding
**Lightbulb**: Major Discovery
**Filled Flag**: Nation Founding
**Book**: Law Established
## Major Events
Below follows a list of only the major events that have taken place throughout the history of Avasar.
```dataview
TABLE WITHOUT ID
date + " - " + title AS "Event",
nation AS "Nation",
description AS "Description"
FROM #timeline_event AND (#major_event OR #world_event) 
WHERE title != ""
SORT date DESC
```
## Events
Below follows a list of all events, minor and major, that have taken place throughout the history of Avasar.
```dataview
TABLE WITHOUT ID
"[[" + date + " - " + title + "]]"
+ choice(contains(file.etags, "#city_founding"), " `far:Flag`", "") 
+ choice(contains(file.etags, "#discovery"), " `far:Lightbulb`", "") 
+ choice(contains(file.etags, "#nation_founding"), " `ris:Flag`", "") 
+ choice(contains(file.etags, "#law"), " `ris:Book2`", "")
+ choice(contains(file.etags, "#war"), " `ris:Sword`", "")
AS "Event",
nation AS "Nation",
description AS "Description"
FROM #timeline_event 
WHERE title != ""
SORT date DESC
```
