Status:: 
Tags:: #🗺️
Links:: [[Personal Knowledge Management MOC]]
___
# Note Taking MOC
## Notes
## Queries
### Notes
```dataview
list from [[Note Taking MOC]] AND !outgoing([[Note Taking MOC]]) AND !#i and !#thoughts
```
### Inputs
```dataview
table Tags as Type, Links, Created
from [[Note Taking MOC]] AND #i
sort Tags desc
```

### Thoughts
```dataview
table Created
from [[Note Taking MOC]] AND #thoughts
sort file.mtime desc
```
___
References:

Created:: 2022-07-09 19:41