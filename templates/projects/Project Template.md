Status:: #🚧/🟥
Tags:: #projects
Links:: [[🚧 My Projects]]
___
# <% tp.file.title %>
Deadline:: <% tp.file.cursor(2) %>
Area:: 
<%*
	const dir = "1. Projects/" + tp.file.title + "/";
	if (!tp.file.exists(dir)) {
		await this.app.vault.createFolder(dir)
	}
	await tp.file.move(dir + tp.file.title)
%>
## Kanbans
```button
name Create Kanban
type command
action QuickAdd: 📌 Create Kanban
```
%%Link the related kanban here%%

## Resources
### Notes
%% Add any non-connected notes or specific contexts here%%

#### Query
```dataview
list
from ([[]] or "1. Projects/<%tp.file.title%>") and !outgoing([[]])
```
### External Links
## Planning
**Objective:**
- 

**Key Results:**
- 

**Obstacles and their solutions:**
- 

**Timeframe:**
%% Include links to related weeks or days %%
- 
## Reflection
**Satisfied?**
- 

**Improvements and solutions learned for the future**:
- 

___
Created:: <%tp.date.now("YYYY-MM-DD HH:mm") %>