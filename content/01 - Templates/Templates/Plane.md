---
tags:
  - plane/
description: 
celestial_body: 
attuned_god: 
aliases:
---
*"QUOTE"*
```dataviewjs
var p = dv.current();
dv.paragraph("**Attuned God:** " + p.attuned_god);
dv.paragraph("**Celestial Body:** " + p.celestial_body);
dv.paragraph("**Alternative Names:** " + p.aliases);
```
## Overview
```dataviewjs
var p = dv.current();
dv.span(p.description)
```
