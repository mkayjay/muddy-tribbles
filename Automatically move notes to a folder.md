---
aliases: Auto Note Mover Plugin
---
Status:: 
Tags:: 
Links:: [[Obsidian Tips]] - [[My Plugins]]
___
# Automatically move notes to a folder
*Doesn't fully render templates if used when creating new files with QuickAdd :/ Will keep thinking of a solution*
## Principles
I use the `Auto note mover` plugin to move notes to a folder based on title or tag.
## Examples
### Move [[Fleeting Notes]] created from [[Fleeting Notes App]]
After turning notes into `#notes/🌲` you can move them into the root folder of the app, away from whatever folder you set to import all fleeting notes.
### Move notes related to a project into the folder
- To help practice archiving notes ^1ba03f
	- Most of the things you're prone to archive are project-based notes that may be one-off things, so I would suggest moving all notes related to a project into the project folder.
	- Once the project is done, you can consider which items to move to archives.
	- Implementation
		- Create a `pNote` tag, create a nested alternative like `#pNote/projectName` 
		- Add a new condition for moving in the plugin for the tag
		- Tag all notes related to project with that
### Quick Archive
Just create a tag that auto moves to archived folder
___
References:

Created:: 2022-10-18 00:10