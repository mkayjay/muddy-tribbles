---
aliases: PKM MOC
---
Status::
Tags:: #🗺️ #resource
Links:: [[📝 My Resources]]
___
# Personal Knowledge Management MOC
## Notes
This contains all the relevant notes I've taken on personal knowledge management :)
### Practices
- [[PARA Method]] to organize knowledge
- [[Maps of Content (MOC)]] to organize notes related to a concept
### Tools
- [[Obsidian MOC|Obsidian MD]] for most of my workflows and knowledge storage
- [[Zettelkasten]]
## Queries
### Notes
```dataview
list from [[Personal Knowledge Management MOC]] AND !outgoing([[Personal Knowledge Management MOC]]) AND !#i and !#thoughts
```
### Inputs
```dataview
table Tags as Type, Links, Created
from [[Personal Knowledge Management MOC]] AND (#i)
sort Tags desc
```

### Thoughts
```dataview
table Created
from [[Personal Knowledge Management MOC]] AND #thoughts
sort file.mtime desc
```
___
References:

Created:: 2022-07-07 00:18