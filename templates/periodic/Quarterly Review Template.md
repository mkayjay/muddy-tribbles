<%tp.file.include("[[Hover Icons for Headers Addon]]")%>
Status:
Tags: #reviews/quarterly
Links: [[📆 My Periodic Reviews]]
___
# <% tp.file.title %>
 [[<% moment(tp.file.title,'YYYY-[Q]Q').subtract(1, 'quarter').format('YYYY-[Q]Q') %>]] ⬅️  [[<%tp.date.now("YYYY")%>]]  ➡️ [[<% moment(tp.file.title,'YYYY-[Q]Q').add(1, 'quarter').format('YYYY-[Q]Q') %>]]

> “Your decisions about allocating your personal time, energy, and talent ultimately shape your life’s strategy.”
## Future Plan
### Action Items
```dataview
task
where file.name = "<%tp.file.title%>"
```
<% tp.file.include("[[Focus Area Addon]]") %>
## Recap
```dataview
table Total as Rating, Summary, Personal, Career
from #reviews/monthly AND [[<%tp.file.title%>]]
sort file.name desc
```
## Reflection

<% tp.file.include("[[templates/periodic/Reflection Addon]]") %>
___
Created:: <% tp.date.now("YYYY-MM-DD HH:mm") %>
