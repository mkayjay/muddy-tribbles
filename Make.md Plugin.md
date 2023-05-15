Status:: 
Tags:: #plugin
Links:: [[Obsidian Community Plugins]]
___
# Make.md Plugin
Summary:: Improves the user experience of folders, tags, and markdown

There's a lot this plugin offers, but only the essentials will be covered. Feel free to explore things like their flow editor as well, and learn more in their [discord community](https://discord.com/invite/BE7dkWDpbM)
- Folders are enhanced through spaces, which let you better section and organize your notes with custom dashboards and tables
- Tags are supercharged with contexts that you let you add metadata fields to your notes, which can then be viewed in different ways through databases you can sort and filter
- Editing notes becomes frictionless with their flow and blink editor
- And lastly, applying markdown becomes simple using slash commands

I personally don't need it since I mostly access everything using the quick switcher or command pallete, and am used to relying on the keyboard for most functionalities, and things like contexts can already be implemented via [[Metadata Menu Community Plugin]].

Nonetheless, it's a very user-friendly interface for actually getting things done and lessening some of the obstacles Obsidian provides.
## Spaces

Spaces can be seen as a customizable file explorer.

You can open it by running the following command, which you can then see in the top left of your left sidebar:
```button
name MAKE.md: Open Spaces
type command
action MAKE.md: Open Spaces
```
^button-bsud

You can
- add sections to store groups of folders
- add emojis associated with certain folders or notes

By clicking on a certain folder, you'll see a new view.

The first tab is the customizable main note for the folder, which you can use to add relevant links or information.

The second tab just shows all the files in the folder, which you can then view in different modes, and also filter and sort to your liking.

You can also create manual views by clicking on the `+ Table`, but I prefer ones that automatically update.

To do so, we can look to use...
## Contexts
Contexts enhance the tags in your vault.

Instead of only being used to classify information, each tag now has it's own fields and becomes its own separate type of note in your vault.

[[🚧 My Projects]], [[📥 My Inputs]], all have their own characteristics thanks to their tag, which you can then update through the [[Metadata]] of your notes.
### Creating a new context
When creating a new kind of note (ex. a note for labs, or a note for textbooks)
- Create a folder for it (ex. [[My Assignments]])
- Create a new tag and create a template with desired metadata fields (ex. `#assignment`)
	- Add frontmatter or in-line metadata fields
- Click on the folder in the `Spaces` view
- Top left, `+` and add the tag
- Sync properties and add it all
- Click on the tag, and change the types of each field to it's proper kind (text, number, link, date, etc)
### Adding a new context note
- Just add a note with the same tag
- I personally use templates though to make it efficient
### View notes of a certain context
```button
name MAKE.md: Open Spaces
type command
action MAKE.md: Open Spaces
```
^button-bsud
- Has a `Contexts` tab you can open, and clicking on a certain tag will show all notes using it
	- See metadata
		- Can switch between different views like board, table, etc
		- Can add filters and sorts
### View contexts related to a note
To view current contexts related to a note
```button
name MAKE.md: Open Context Explorer
type command
action MAKE.md: Open Context Explorer
```
^button-6m43

Can use it to edit and add metadata as well !
## Blink
To quickly edit notes that show up from a search, you can replace the current quick switcher with Blink mode:
```button
name MAKE.md: Blink
type command
action MAKE.md: Blink
```
^button-sh7n
## Flow
Flow Mode lets you edit your notes from practically anywhere.
### Flow Links
Here's a normal embed link:
![[Example Note#Example Note]]

When hovering over the embed, you can choose to "Toggle Flow", which will let you edit the embed from inside this file.

You can also create flow embeds by prefixing normal links with !!
___
Created:: 2023-01-20 21:35