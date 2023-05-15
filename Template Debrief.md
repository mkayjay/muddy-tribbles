Status::
Tags::
Links:: [[Vault Overview]]
___
# Templates Debrief
> [!INFO] Template Explanations
> Learn the anatomy of each template [[Template Explanations|here]] and their workflows [[My Workflows|here]]

This vault uses the [[My Plugins#Templater|Templater]] plugin to allow for extreme customization using code snippets which look like `<% bla bla bla %>`

One of these commands is `<%tp.file.title%>`, which gets turned into the note title upon file creation to help with querying. If you change the title later, you will have to manually update this to maintain the queries.
## Choices
[[Showing inline titles]]
## Questions
### How to add templates into vault?
Watch this video to learn how to import and use your templates:
https://youtu.be/7JMRrskgw7I?t=67
### How to use templates?
- To keep things simple I use the `quickadd` community plugin
	- To create a new note or new project, open command pallete and run the `Quickadd: Run Quickadd` command via `Ctrl + Shift + P`
- `Ctrl + Shift + T` to add a template to the current file
### How to modify existing templates?
- To modify the template selection process, go to quickadd settings, `Manage Macros`, and you will see the already existing quickadd
- Find `/templates` folder and just edit the text, structure, and queries to your liking :) My templates are only examples, and are not the "absolutely correct" way to do things- feel free to add in snippets that compliment your own daily routines and workflows!
### How can I add partial templates?
- [[My Addons]]
## Anatomy
### tp.file.cursor
`<% tp.file.cursor %>` are just jump points for the cursor, which you can jump to by pressing `Alt+8` or using the command `Jump to next cursor location`
### What do I put for status, tags, and links?
*Disclaimer: This is my personal interpretation and use case*
#### Status
Denotes the development of a note, which can then be used to query and create kanban boards to visualize progress
##### Examples
[[My Inputs Workflow#Status]]

[[Managing and growing evergreen notes#Status]]
#### Tags
- Tags that may be used for querying and for adding the specific type of note
	- ex) the different kinds of inputs like `i/article` and `i/book`
#### Links
- Links to parent notes of the current note, both conceptually and in relation to your own life
- ex) A `Soccer` note could have a `Sports` link or a `Hobbies` link
### Why are there double colons?
- It converts the content after the colon into metadata, which can then be displayed and used in dataview queries. See the [[MOC Template]] queries for examples
### Why are notes sorted by file.mtime?
- Tables will show the date of creation, but will be sorted at their latest modified time to allow for notes that were created a long time ago but are still used frequently
## Troubleshooting
### Templater commands aren't loading fully
ex) `<%tp.file.title%>` and `<%tp.date.now("YYYY-MM-DD")%>`

If the templates don't automatically load upon note creation, be sure to enable the `Trigger Templater file on new file creation` setting in the `Templater` community plugin

If you manually import the templates each time via hotkey, then you might need to run a command to trigger the templates (you can manually do it by opening command pallete `Ctrl/Cmd + P` and then typing in `Replace templates in the active file`)
___
References:

Created:: 2022-07-06 22:34