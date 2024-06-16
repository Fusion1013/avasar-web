---
tags:
  - plane/material
description: A dark mirror of the material plane
celestial_body: "[[Cosmology Overview#Sahti (Dark)|Sahti]]"
attuned_god: N/A
aliases:
  - The Eternal Twilight
  - Noctus
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
