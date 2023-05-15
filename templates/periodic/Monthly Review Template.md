<%tp.file.include("[[Hover Icons for Headers Addon]]")%>
Status:
Tags: #reviews/monthly
Links: [[📆 My Periodic Reviews]]
___
# <% tp.file.title %>
[[<% moment(tp.file.title, "YYYY-[M]MM").add(-1, 'months').format("YYYY-[M]MM") %>]] ⬅️ [[<% moment(tp.file.title,'YYYY-[M]MM').format('YYYY-[Q]Q') %>]]  ➡️ [[<% moment(tp.file.title, "YYYY-[M]MM").add(1, 'months').format("YYYY-[M]MM") %>]]
> “Your decisions about allocating your personal time, energy, and talent ultimately shape your life’s strategy.”
## Future Plan

### Action Items
```dataview
task
where file.name = "<%tp.file.title%>"
```

<%tp.file.include("[[templates/periodic/Focus Area Addon]]") %>
## Recap
```dataview
table Total as Rating, Summary, Personal, Career
from #reviews/weekly AND [[<%tp.file.title%>]]
sort file.name asc
```
### Key Metrics
#### Energy
```tracker
searchType: dvField
searchTarget: Physical, Mental, Emotional, Spiritual
folder: /dailyNotes
startDate: <% moment(tp.file.title,'YYYY-[M]MM').startOf('month').format('YYYY-MM-DD') %>
endDate: <% moment(tp.file.title,'YYYY-[M]MM').endOf('month').format('YYYY-MM-DD') %>
summary:
    template: "AVERAGES\nPhysical: {{average(dataset(0))}}\nMental: {{average(dataset(1))}}\nEmotional: {{average(dataset(2))}}\nSpiritual: {{average(dataset(3))}}\n"
```
``` tracker
searchType: dvField
searchTarget: Physical, Mental, Emotional, Spiritual
datasetName: Physical, Mental, Emotional, Spiritual
folder: /dailyNotes
month:
    startWeekOn: 'Sun'
    threshold: 7, 7, 7, 7
    color: green
    dimNotInMonth: false
    todayRingColor: white
    selectedRingColor: steelblue
    circleColorByValue: true
    showSelectedValue: true
    initMonth: <% moment(tp.file.title, "YYYY-[M]MM").format("YYYY-MM") %>
```
#### Habits
##### Meditation
``` tracker
searchType: task.done, task.notdone
searchTarget: Meditate, Meditate
folder: /dailyNotes
datasetName: Meditate, Not Meditate
month:
    color: green
    todayRingColor: white
    selectedRingColor: steelblue
    showSelectedValue: false
    initMonth: <% moment(tp.file.title, "YYYY-[M]MM").format("YYYY-MM") %>
```

``` tracker
searchType: task.done, task.all
searchTarget: Meditate, Meditate
folder: /dailyNotes
startDate: <% moment(tp.file.title,'YYYY-[M]MM').startOf('month').format('YYYY-MM-DD') %>
endDate: <% moment(tp.file.title,'YYYY-[M]MM').endOf('month').format('YYYY-MM-DD') %>
summary:
    template: "Meditate - {{sum(dataset(0))/sum(dataset(1))*100}}% - {{sum(dataset(0))}}/{{sum(dataset(1))}} Days Completed"
```
## Reflection

<%tp.file.include("[[templates/periodic/Reflection Addon]]") %>

___
Created:: <% tp.date.now("YYYY-MM-DD HH:mm") %>
