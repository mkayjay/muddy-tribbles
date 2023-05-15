Status:: 
Tags:: 
Links:: [[🏠 My Home]]
___
# ♻️ My Habits
For [[Creating and tracking your own habits and statistics]]
## Statistics
### Energies
```tracker
searchType: dvField
searchTarget: Physical, Mental, Emotional, Spiritual
folder: /dailyNotes
summary:
    template: "AVERAGES\nPhysical: {{average(dataset(0))}}\nMental: {{average(dataset(1))}}\nEmotional: {{average(dataset(2))}}\nSpiritual: {{average(dataset(3))}}\n"
```
``` tracker
searchType: dvField
searchTarget: Physical, Mental, Emotional, Spiritual
datasetName: Physical, Mental, Emotional, Spiritual
folder: /dailyNotes
month:
    mode: annotation
    startWeekOn: 'Sun'
    threshold: 7, 7, 7, 7
    color: white
    dimNotInMonth: false
    annotation: 💪,🧠,😊,🙏
    showAnnotationOfAllTargets: true
```
## Habits
### Meditation
#### Total
``` tracker
searchType: task.done, task.all
searchTarget: Meditate, Meditate
folder: /dailyNotes
summary:
    template: "Meditate - {{sum(dataset(0))/sum(dataset(1))*100}}% - {{sum(dataset(0))}}/{{sum(dataset(1))}} Days Completed"
```
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
```
___
References:
