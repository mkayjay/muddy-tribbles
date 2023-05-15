
<%tp.file.include("[[Hover Icons for Headers Addon]]")%>
Status:
Tags: #reviews/yearly
Links: [[📆 My Periodic Reviews]]
___
# <% tp.file.title %>
 [[<% moment(tp.file.title,'YYYY').subtract(1, 'year').format('YYYY') %>]] ⬅️ This Year ➡️  [[<% moment(tp.file.title,'YYYY').add(1, 'year').format('YYYY') %>]] 

> “Your decisions about allocating your personal time, energy, and talent ultimately shape your life’s strategy.”
## Future Plan
### Action Items
```dataview
task
where file.name = "<%tp.file.title%>"
```

### New Years Resolution
Objective:

Key Results:

I will accomplish this by...
- 

Related projects:
- 

<%tp.file.include("[[templates/periodic/Focus Area Addon]]") %>
## Recap
```dataview
table Total as Rating, Summary, Personal, Career
from #reviews/quarterly AND [[<%tp.file.title%>]]
sort file.name desc
```
## Reflection
<%tp.file.include("[[templates/periodic/Reflection Addon]]") %>
___
Created:: <% tp.date.now("YYYY-MM-DD HH:mm") %>
