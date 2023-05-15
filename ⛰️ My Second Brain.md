Tags:: #area
Links:: [[⛰️ My Areas]]
___
# ⛰️ My Second Brain
## Queries
### Projects
```dataview
table Deadline
FROM #🚧 AND [[⛰️ My Second Brain]]
SORT Deadline asc
```
### Inputs
```dataview
table Status, Author
FROM #i AND [[⛰️ My Second Brain]]
SORT file.mtime desc
```
### Notes
```dataview
table Created
FROM [[⛰️ My Second Brain]] AND !#🚧 AND !#📥
SORT file.mtime desc
```

___

Created:: 2022-07-11 22:00