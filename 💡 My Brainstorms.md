Tags:: #🔍 
Links:: [[🏠 My Home]]
___
# 💡 My Brainstorms
Uses the [[Brainstorming Template]] to flesh out ideas, whether it be for personal understanding or creating content :) A synthesized version of Andy's Workflow.

Need ideas? See [[Retrieving information from your notes]]

For a more applied approach, consider implementing the [[Applied Brainstorming Addon]]

```button
name Create Brainstorm
type command
action QuickAdd: 💡 Create Brainstorm Note
```
### Backlog #💡/🟥 
```dataview
table Created
FROM #💡/🟥 
where file.name != "💡 My Brainstorms"
sort file.mtime desc
```
### Active #💡/🟨 
```dataview
table Created
FROM #💡/🟨 
WHERE file.name != "💡 My Brainstorms"
sort file.mtime desc
```
### Finished #💡/🟩
```dataview
table Created
FROM #💡/🟩
WHERE file.name != "💡 My Brainstorms"
sort file.mtime desc
```
___