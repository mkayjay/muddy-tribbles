Tags:: #🔍
Links:: [[🏠 My Home]]
___
# 📚 My Books
## Kanban
### Not Started
```dataview
table started, finished, rating
FROM #📥/🟥 and #i/book
SORT started desc
```
### Consuming Media
```dataview
table started, finished, rating
FROM #📥/🟧 and #i/book
SORT started desc
```
### Implementation
```dataview
table started, finished, rating
FROM #📥/🟨 and #i/book
SORT started desc
```
### Finished
```dataview
table started, finished, rating
FROM #📥/🟩 and #i/book

SORT started desc
```
### Incomplete
```dataview
table started, finished, rating
FROM #📥/⬛ and ![[) Courses]] and ![[' Classes]]

SORT started desc
```