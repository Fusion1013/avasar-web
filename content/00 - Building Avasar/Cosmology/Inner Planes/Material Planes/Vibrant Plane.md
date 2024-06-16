---
tags:
  - plane/material
description: A vibrant mirror of the material plane
celestial_body: "[[Cosmology Overview#Aurius (Light)|Aurius]]"
attuned_god: N/A
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
