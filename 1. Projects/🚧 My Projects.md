Tags:: #🔍
Index:: [[🏠 My Home]]
___
# 🚧 My Projects

```button
name Create Project
type command
action QuickAdd: 🚧 Create Project
```
### Backlog #🚧/🟥 
```dataview
table Deadline, Area
FROM #🚧/🟥 AND !"templates" AND !"4. Archives"
WHERE file.name != "🚧 My Projects"
SORT Deadline asc
```
### Active #🚧/🟨
```dataview
table Deadline, Area
FROM #🚧/🟨 AND !"4. Archives"
WHERE file.name != "🚧 My Projects"
SORT Deadline asc
```
### Finished #🚧/🟩
```dataview
table Deadline, Area
FROM #🚧/🟩 AND !"4. Archives"
WHERE file.name != "🚧 My Projects"
SORT Deadline asc
```
### Archived #🚧/⬛
```dataview
table Deadline, Area
FROM #🚧/⬛ AND !"4. Archives"
WHERE file.name != "🚧 My Projects"
SORT asc
```
___