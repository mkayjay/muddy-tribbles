---
limit: 100
mapWithTag: true
icon: clipboard-list
tagNames: 
excludes: 
extends: 
---

Area:: {"type":"File","options":{"dvQueryString":"dv.pages(\"#area\")\n.filter(p => !p.file.path.includes('templates'))\n.filter(p => !p.file.path.includes('fileClass'))"}}
Deadline:: {"type":"Date","options":{"dateFormat":"YYYY-MM-DD","defaultInsertAsLink":"false","dateShiftInterval":"7 days"}}