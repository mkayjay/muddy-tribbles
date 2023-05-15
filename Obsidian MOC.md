Status:: 
Tags:: #🗺️
Links:: [[Personal Knowledge Management MOC]]
___
# Obsidian MOC
## Notes
### Personal use cases
- [[My Plugins]]
- [[Obsidian Community Plugins]]
- [[My Hotkeys]]
- [[Obsidian Tips]]
## Queries
### Notes
```dataview
list from [[Obsidian MOC]] AND !outgoing([[Obsidian MOC]]) AND !#i and !#thoughts
```
### Inputs
```dataview
table Tags as Type, Links, Created
from [[Obsidian MOC]] AND #i
sort Tags desc
```

### Thoughts
```dataview
table Created
from [[Obsidian MOC]] AND #thoughts
sort file.mtime desc
```
___
References:

Created:: 2022-07-07 21:34