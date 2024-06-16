---
alias: 
- Saxum Sovereignty
- Saxum
tags:
- nation

todo: Flesh out the organizations section
editors: Fusion
---
*"Leave those shattered plains behind"*

**Government:** A [[The Saxum Triumvirate|Triumvirate]] of three mages, along with a council of 13 representatives.
**Languages:** [[Old Taundorian]]
## Overview
Sheltered from the rest of the world by the towering [[Dragonback Mountains]] and Fracrish Mountains, the Saxum Sovereignty is a small but prosperous nation. This landscape of towering mountains and flowing hills is known for its gray skies, fits of cold rain, and occasional snowfall. The [[Dragonback Mountains]] and [[Fracrish Mountains]] shield the people from most of the threats that loom beyond the boundaries of the nation.
## History
The Saxum Sovereignty was [[1185 APC - Saxum Sovereignty Founding|founded in 1185 APC]], not long after the cataclysm that formed the now Turochan Kingdom. Due to the new nation's anti-magic stance, practitioners of magic were hunted and banished from the kingdom. Some of these people undertook the perilous journey through the Fracrish Mountains, to the valley that now forms the Saxum Sovereignty. With the founding of the capital, this valley soon became a safe haven for practitioners of arcane and divine magic.

Relations with the Turochan Kingdom are still tense, but have significantly calmed since the earlier days. Trade has started to open up more and more over the last 20 years, as Turochan has started to relax their anti-magic policies. The construction of a major trade route through the mountains has significantly aided in these efforts. Information of magical nature is still being kept behind closed doors however.
## Major Cities
There are only four major cities in Saxum.
```dataview
TABLE description AS "Description"
FROM #city
WHERE nation = "Saxum"
```
## Major People
```dataview
TABLE
description AS "Description",
race AS "Race",
(age + " years") AS "Age"
FROM #major_person AND #saxum_sovereignty AND #alive
```
## Major Organizations
```dataview
TABLE
description AS "Description"
FROM #organization/major
WHERE contains(nation, "Saxum Sovereignty")
```
## Magical Society
Even though this nation was founded on the idea of allowing free use of magic, there is no academy focused primarily on magic within this nation. Instead, magical knowledge is taught in almost every school, starting at an early age. This way almost everyone living within the nation knows at least some magic. There are a few research institutes that allow for higher study of the arcane, though they rely heavily on self-study and research.

While mundane magic is commonly used for everyday activities, there are only a few hundred practitioners of high level magic. These individuals are often nobles living in the capital of [[Gulstad, City of Gold|Gulstad]], or people in other positions of power.
## Religion
In the nation of Saxum, a staunchly secular society prevails, where the very mention of religion is met with suspicion and disdain. Major cities have become breeding grounds for a deep-seated anti-religious sentiment, where discrimination against the faithful is an unfortunate and common occurrence. This oppressive atmosphere extends to every corner of urban life, with city guards themselves participating in the systemic prejudice, leaving those who seek solace in faith to live in the shadows. The government, seemingly unwilling to address this growing issue, allows this discriminatory culture to fester unchecked, making for a society where belief in the divine is met with cold hostility and mistrust.

The worship of certain gods, those deemed unsafe by the ruling [[The Saxum Triumvirate|Saxum Triumvirate]], has been forcefully outlawed. Among these deities, the figure of [[Irellia, Peace|Irellia, the Godess of Peace]], stands as a forbidden symbol of devotion. The consequences of defying these religious proscriptions are severe, with punishment ranging from imprisonment to banishment. In a land where faith is tightly controlled, even the prayerful whisper of her name can carry profound consequences, leading devotees of [[Irellia, Peace|Irellia]] to practice their faith in secret, hidden away from the scrutinizing gaze of [[The Saxum Triumvirate|The Triumvirate]] and the city guards.
## Economy
### Coin Designs
The coins have the current members of [[The Saxum Triumvirate]] on the front of them, surrounded by their names and the date the individual coin was printed, two numbers on each side. The individual that has been on the council the longest is on the platinum, the second longest on the gold, and the last on the silver coin. The current coins have the following names on them:
- Platinum: [[Archmage Igorim Ovras|Igorim Ovras]]
- Gold: [[Master Leo Umbras|Leo Umbras]]
- Silver: [[Ezorah von Abendroth]]
The backs of the coins feature the symbol of the [[Irellia, Peace|Goddess of Peace, Irellia]], engulfed in flames. Surrounding it are 8 symbols representing the different schools of magic.
## Timeline
```dataview
TABLE WITHOUT ID
"[[" + date + " - " + title + "]]"
+ choice(contains(file.etags, "#city_founding"), " `far:Flag`", "") 
+ choice(contains(file.etags, "#discovery"), " `far:Lightbulb`", "") 
+ choice(contains(file.etags, "#nation_founding"), " `ris:Flag`", "") 
+ choice(contains(file.etags, "#law"), " `ris:Book2`", "")
AS "Event",
description AS "Description"
FROM #timeline_event 
WHERE contains(nation, "Saxum Sovereignty")
SORT date DESC
```
