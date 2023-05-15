Status::
Tags:: 
Links:: [[Vault Overview]] - [[Obsidian Community Plugins]]
___
# My Plugins
## Principles
I already imported the required plugins (dataview, templater, etc) to use the templates and workflows so you can play around with adjusting and importing them into new notes.

**Each plugin has a documentation page, go to Settings > Community Plugins > Click on the plugin title**

I try to explain what plugins I use and for what purpose in each workflow, but if you want to modify them then I'd recommend reading their respective documentations or external tutorials.

I personally use all of the quality of life plugins in my main vault, but only some are installed.

## Required
### Buttons
- Makes it more convenient to create new notes while in the respective query note
- When you click one of the create buttons with something in your clipboard, it uses it as the title
	- example use case: after creating a project, copy header title then click on create kanban
- If the name of the command changes, be sure to modify the name of the command as well
### Calendar
- Helps easily create and open daily/weekly notes through its side bar pane by clicking on the date
	- Be sure to create the respective notes on the same day or else the templater stuff will mess up :(
	- The `W` column is for weekly notes
### [[Dataview Plugin]]
### Folder Note
- Ctrl + click to create a folder note
	- Whenever you open that folder, you will see the note pop up
	- Folder note mostly contains a visual representation of its contents
### Kanban
- Main task management for projects
### [[Make.md Plugin]]
### [[QuickAdd Plugin|QuickAdd]]
- A centralized command palette for custom workflows
- Tons of customizability, especially if you inject your own scripts, so let your imagination run wild B)
- I just mainly use it to organize the different templates and use cases of the vault, like creating the different relevant notes
### Templater
- Default templates on steroids
- Features include
	- Jumping to set cursor locations using <%tp.file.cursor(`number`)%>
	- Setting a default template that automatically loads on root/folder notes
	- Internal variables like dates, titles, etc
- Pretty much the backbone of all templates
	- especially weekly templates as it has to link to all the previous week's notes
### Tracker
- Tracking things like statistics in the daily note to be graphed in weekly reviews
	- ex) Energy levels
## Appearance
If you're a fan of customizing your own theme, then the Minimal Theme is all you need. It's like a no-code solution.
### Minimal Theme Settings
- Includes preset color schemes and toggles for different visual settings
### Style Settings
- Ultimate customization
- Change CSS design and colors of background, headers, text, etc
## Quality of Life
### Auto Note Mover
- Can move notes based on tags or title using regex
### Completed Task Display
- Can toggle on/off on the sidebar
### Copy Block Link
- Copies blocks if you don't have headers
### Customizable Sidebar
- Clean the sidebar so you can include the commands you frequently use :)
### Emoji Toolbar
- Quick access to emojis using `Ctrl+Shift+E` to spice up your notes ;)
### File Tree Alternative
- View contents of notes, "zoom in" on select folders, fold/collapse all
### Hide Sidebars When Narrow
### Highlightr
- Different colored highlights ;)
### Linter
- Formats code on save to keep notes consistent
- Formats on save
### Outliner
- Modifies the way you outline and gives more hotkeys
### Obsidian42 - BRAT
- Can use non-published community plugins without them being released
### Natural Language Dates
- Can use @today, etc

### Paste URL into selection
- Normally when you select text and paste something, it will replace the selected with the pasted
- However, this plugin converts it into a markdown link
### Recent Files
- Self-explanatory
### Smart Random Note
- Has a command to open a random note based on current search query (see dice icons on left toolbar)
___
References:

Created:: 2022-07-07 20:29