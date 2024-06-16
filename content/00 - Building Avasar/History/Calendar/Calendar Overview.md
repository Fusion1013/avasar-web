# Calendar Overview
## Overview
The year is split into 653 days, or 16 months. All months have 41 days, except for [[Zermid]] which has 38 days.
## Days of the Week
The names for the days of the week are based on the names for the major celestial bodies, in order from Taiya. There are 5 weeks/month.
```dataview
TABLE WITHOUT ID
(day_order + 1) + ": [[" + file.name + "]]" AS "Day Name",
astral_body AS "Astral Body"
FROM #week_day 
SORT day_order ASC
```
### Months
The names for the months have their roots from the names of the gods, with influences from [[Proto-Naiwa]].
```dataview
TABLE WITHOUT ID
(order + 1) + ": [[" + file.name + "]]" AS "Month Name",
god AS "God"
FROM #month 
SORT order ASC
```
