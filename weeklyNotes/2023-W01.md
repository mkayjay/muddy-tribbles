<%tp.file.include("[[Hover Icons for Headers Addon]]")%>
Status:
Tags: #reviews/weekly
Links: [[📆 My Periodic Reviews]]
___
# <% tp.file.title %>
[[<% moment(tp.file.title, "YYYY-[W]WW").add(-1, 'weeks').format("YYYY-[W]WW") %>]] ⬅️ [[<% moment(tp.file.title,'YYYY-[W]WW').format('YYYY-[M]MM') %>]] ➡️ [[<% moment(tp.file.title, "YYYY-[W]WW").add(1, 'weeks').format("YYYY-[W]WW") %>]]
## Future Plan
### Action Items
```dataview
task
where file.name = "<%tp.file.title%>"
```
### Projects
```dataview
table deadline, area
FROM [[<% moment(tp.file.title,'YYYY-[W]WW').add('1', 'weeks').format("YYYY-[W]WW") %>]] AND #projects
WHERE file.name != "Project Template"
SORT deadline asc
```
## Recap
### Days

```dataview
table Rating as ⭐, Sentence as Summary, Story, headings as ✍️
from [[<%tp.file.title%>]] AND "dailyNotes"
sort file.name asc
```
### Key Metrics
#### Energy
``` tracker
searchType: dvField
searchTarget: Physical, Mental, Emotional, Spiritual
folder: /dailyNotes
startDate: <% moment(tp.file.title,'YYYY-[W]WW').day(1).format("YYYY-MM-DD") %>
endDate: <% moment(tp.file.title,'YYYY-[W]WW').add(1,'weeks').day(0).format("YYYY-MM-DD") %>
line:
    title: Energy
    yMax: 10
    yAxisLabel: Phys (R) / Ment (B) Emot (Y) / Spir (G)
    lineColor: red, blue, yellow, green
```
```tracker
searchType: dvField
searchTarget: Physical, Mental, Emotional, Spiritual
folder: /dailyNotes
startDate: <% moment(tp.file.title,'YYYY-[W]WW').day(1).format("YYYY-MM-DD") %>
endDate: <% moment(tp.file.title,'YYYY-[W]WW').add(1,'weeks').day(0).format("YYYY-MM-DD") %>
summary:
    template: "AVERAGES\nPhysical: {{average(dataset(0))}}\nMental: {{average(dataset(1))}}\nEmotional: {{average(dataset(2))}}\nSpiritual: {{average(dataset(3))}}\n"
```

Was there any lacking energy? If so, how can I work on improving it this upcoming week?
- 

### Projects
```dataview
table deadline as Deadline, area as Area
FROM [[<% moment(tp.file.title,'YYYY-[W]WW').format("YYYY-[W]WW") %>]] AND #projects
WHERE file.name != "Project Template"
SORT deadline asc
```
#### Tasks
```dataview
TABLE WITHOUT ID 
regexreplace(Tasks.text, "@\[.*$", "") as Task,
meta(Tasks.section).subpath as "Status",
file.link as "Board"
from "1. Projects"
where kanban-plugin = "basic"
FLATTEN file.tasks As Tasks
WHERE contains(Tasks.text, "<% moment(tp.file.title,'YYYY-[W]WW').day(1).format("YYYY-MM-DD") %>") OR   
contains(Tasks.text, "<% moment(tp.file.title,'YYYY-[W]WW').add(-1,'weeks').day(2).format("YYYY-MM-DD") %>") OR 
contains(Tasks.text, "<% moment(tp.file.title,'YYYY-[W]WW').add(-1,'weeks').day(3).format("YYYY-MM-DD") %>") OR 
contains(Tasks.text, "<% moment(tp.file.title,'YYYY-[W]WW').add(-1,'weeks').day(4).format("YYYY-MM-DD") %>") OR 
contains(Tasks.text, "<% moment(tp.file.title,'YYYY-[W]WW').add(-1,'weeks').day(5).format("YYYY-MM-DD") %>") OR 
contains(Tasks.text, "<% moment(tp.file.title,'YYYY-[W]WW').add(-1,'weeks').day(6).format("YYYY-MM-DD") %>") OR contains(Tasks.text, "<% moment(tp.file.title,'YYYY-[W]WW').add(1,'weeks').day(0).format("YYYY-MM-DD") %>")

SORT date(Tasks.due.file.name)
```
## Reflection
### Summary

### Biggest Personal Achievement

### Biggest Career Achievement

### Learning Review
**3 great things that happened to me last week were**
- 

**The main struggle I faced this week was...**
- 

**and if I were advising or mentoring someone dealing with the same struggle, I'd advise them to...**
- 

**2 things I learned about myself this past week include...**
- 

**2 things I learned about others include...**
- 

**1 decision I could have made last week to make my life better or to move ahead faster would have been...**
- 

### Life Review
> Rate from 1-5, then multiply the total sum by 2

**Health:**

**Productivity:**

**Mental Wellbeing:**

**Learning:**

**Relationships:**

**Goals:**

**Experiences:**

**Energy:**

**Finances:**

**Courage/Spirit:**

Total:: 

**What can I try and improve on this week?**

### Focus
**Did you complete what you set out to do previously? Are you content with your productivity?**

**Does your calendar (and commitments) match your priorities and values?**

**Did I do something outside of my plans? How did it influence the week?**
### Time Management
**Could you have spent more time on something?**

**Could you have spent less time on something?**

**Advice for the future?**

### Troubleshooting
**System/Tool-related issues?**

**Workflow/Routine related?**
- Morning
- Night

**Habit related?**

**Anything else?**

___

Created:: <% tp.date.now("YYYY-MM-DD HH:mm") %>
