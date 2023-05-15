Tags:: #🔍
Links:: [[🏠 My Home]]
___
# 📥 My Inputs

Refer to  [[My Inputs Workflow]]

```button
name Add Input
type command
action QuickAdd: 📥 Add General Input
```
## Inputs Sorted

### No Status
```dataview
table started, rating, source
FROM #📥/ AND !"templates" AND !"fileClass" 
SORT started desc
```

### Not Started
```dataview
table started, rating, source
FROM #📥/🟥 AND !"templates" AND !"fileClass"
SORT started desc
```
### Consuming Media
```dataview
table started, rating, source
FROM #📥/🟧 AND !"templates" AND !"fileClass"
SORT started desc
```
### Implementation
```dataview
table started, rating, source
FROM #📥/🟨 AND !"templates" AND !"fileClass"
SORT started desc
```
### Finished
```dataview
table started, finished, rating, source
FROM #📥/🟩 AND !"templates" AND !"fileClass"
SORT started desc
```