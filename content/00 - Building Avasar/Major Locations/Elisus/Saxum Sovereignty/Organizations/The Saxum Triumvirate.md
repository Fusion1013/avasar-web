---
tags:
  - organization/major
nation:
  - Saxum Sovereignty
description: The Saxum Triumvirate is composed of three powerful mages who rule over the Saxum Sovereignty from within the Myriad, located in the capital of [[Gulstad, City of Gold|Gulstad]]. They are [[Archmage Igorim Ovras|Igorim Ovras]], [[Master Leo Umbras]], and [[Ezorah von Abendroth]]. As the ruling body of the nation, they hold ultimate power over all aspects of governance and policy, though they are advised by a council of 13 representatives from different regions of the country. The Triumvirate is known for their formidable magical abilities and their unwavering commitment to Saxum and its prosperity.
---

*"Through our leadership, Saxum will thrive and endure"*
## Overview
```dataviewjs
var p = dv.current();
dv.span(p.description)
```
## History
The [[Saxum Sovereignty Overview|Saxum Sovereignty]] owes its existence to the [[1185 APC - Saxum Sovereignty Founding|founding of the Triumvirate, in the year of 1185 APC]]. The Triumvirate was formed by a group of mages who had fled the newly-formed [[Turochan Kingdom Overview|Turochan Kingdom]] which had banned the use of magic. These mages did not want to be persecuted, and so they created the Triumvirate as a ruling body for a new nation where magic would be accepted and celebrated. Over time, the Triumvirate would become the de facto rulers of this new nation, which became known as the [[Saxum Sovereignty Overview|Saxum Sovereignty]].

The Triumvirate was founded by the mages [[Archmage Igorim Ovras|Igorim Ovras]], [[The Saxum Triumvirate#Yosif Halstrom|Yosif Halstrom]], and [[The Saxum Triumvirate#Celeste Krystof|Celeste Krystof]]. These three mages worked together to establish a new government structure in the aftermath of the cataclysm that destroyed Taundor. Over the years, the membership of the Triumvirate has changed, with new members being appointed as old ones passed away or retired. See the [[The Saxum Triumvirate#Members|Members]] section below for a complete list of all previous and current members.

Throughout its history, the Saxum Triumvirate has faced numerous challenges and crises, including rebellions, and external threats from neighbouring nations. However, the Triumvirate has always managed to overcome these challenges and emerge stronger and more united than before.
## Members
Below follows a list of the most notable members of the Triumvirate, with a short description for each. For more information about the current members, see the attached links to their separate pages.
### Previous Members
```dataview
TABLE
description AS "Description",
choice(contains(file.etags, "#alive"), "Alive", "Dead") AS "Status"
FROM #major_person AND #saxum_triumvirate AND -#saxum_triumvirate_current_member 
```
### Current Members
```dataview
TABLE
description AS "Description",
choice(contains(file.etags, "#alive"), "Alive", "Dead") AS "Status"
FROM #major_person AND #saxum_triumvirate AND #saxum_triumvirate_current_member 
```
## The Council
The Council of the [[Saxum Sovereignty Overview|Saxum Sovereignty]] is made up of thirteen representatives, each chosen by their respective regions. They serve as advisers to the Saxum Triumvirate, providing counsel and offering insight into the needs and concerns of their constituents. The council meets regularly within the [[Gulstad, City of Gold#The Myriad|Myriad]], discussing matters of policy, law, and governance, and voting on matters that require their collective approval.

Each member of the council is expected to represent the interests of their region and its people, but they must also work together for the good of the entire nation. The council members are respected leaders within their communities, known for their wisdom, experience, and dedication to the betterment of the [[Saxum Sovereignty Overview|Saxum Sovereignty]].
### Council Members
```dataview
TABLE
description AS "Description"
FROM #saxum_council AND #alive 
SORT file.name ASC
```
