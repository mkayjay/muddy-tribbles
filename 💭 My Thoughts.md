Tags:: #🔍
Links:: [[_index]]
___
# My Thoughts
- Consider using thoughts as inputs that can create/add onto already existing notes
## Categories
#💭/memories  
- anecdotes and experiences

#💭/reflections   
- personal thoughts and lessons

#💭/musings   
- random shower ideas
### Memories 
```dataview
table Created
from #thoughts/memories
where file.name != "💭 My Thoughts"
sort Created desc
```
### Reflections 
```dataview
table Created
from #thoughts/reflections
where file.name != "💭 My Thoughts"
sort Created desc
```
### Musings 
```dataview
table Created
from #thoughts/musings
where file.name != "💭 My Thoughts"
sort Created desc
```
## All Unsorted
```dataview
list
from #thoughts/
where file.name != "= Thoughts"
sort Created desc
```
___