Status:: 
Tags:: #plugin
Links:: [[Metadata]] - [[Obsidian Community Plugins]]
___
# Metadata Menu Community Plugin

> [!INFO] Video overview of features by yours truly ;)
> https://www.youtube.com/watch?v=7o9j7WJfhi0

## Dev's Pitch
Note **Supercharged tags**: Bind tags with fileClass definition. When you put a supercharged tag anywhere in a note, all fields defined in its fileClass definition are available for this note.  
Create a supercharged tag: from existing or not yet exisiting tags  
Add **multiple fileClass and supertags** per note: combine fileClass, supercharged tags and fileclass queries to finegrain-grain which metadata fields are available for your note.There’s a priority management If the same field is defined in serveral fileclasses.  
New **Note’s metadata fields form**: access all available metadata fields for your note in a sigle form where you can easily:
-   insert (at cursor or at a chosen section or at the end of the frontmatter section) a field
-   update a field
-   see which fileclass/supertag the field belongs to
-   change the field settings
-   add a new field definition to one of the supercharged tag/fileclass of this note (it will therefore be available for other notes sharing the same supercharged tags and fileclasses)

For notes with a supercharged tag/fileclass definition, a **Note’s metadata button** will be added right next to the note’s link/tab header/file/backlink/star-result/search-result/… to access the note’s metadata form without opening the note or navigating in the context menu.  
The Note’s metadata button **icon can be customized** in the fileClass definition (from lucide.dev icons set). You can customize where these buttons are displayed or hidden in the settings.  

When used in combination with the Supercharged links plugin, you get a great understanding of what a note is about and great ease to manipulate its metadata from anywhere in your vault.

## Principles
A plugin to allow:
- Notion-like tables where you can edit metadata via the table and other places without directly modifying the text
- Tana supertags where you can set up metadata for a note just by adding a tag
- Preset recommendations for each metadata based on the schema of a fileClass

### Setting up Schemas via fileClass
- [Video](https://www.youtube.com/watch?v=QxXSuh7HUZY&ab_channel=MathieuDelobelle)

A `fileClass` outlines the metadata fields of a note, and to apply this structure, you can add a tag with the `fileClass` name

Whenever you add the tag (ex. `#person`), it will refer to the `fileClass` with the same name.

For example,  [[personn]]  is a `fileClass` has 3 fields of `age`, `interests`, and ``

Setup a `fileClass`
- First, create a folder to store all fileClasses
- Set the folder in the plugin's settings, `Class Files path`
- Create a new note inside the folder with the name of the new fileClass, or go to any note that isn't one -> three dots -> `Add a new file class`

#### Allow for supertags (two options):
- Open the note -> 3 dots in the top right -> Manage fields
	- Map `name` with tag to allow so you can implement the fileClass using `#name` in a new note
- OR include the following in the metadata of the note:
```
---
mapWithTag: true
---
```

If there's overlap of metadata from using multiple `fileClasses` in one note, then it will prioritize the last tag.
#### Nested Supertags
ex) `#i/podcast` via [[fileClass/i/podcast]]

Create a folder inside your fileClass file of the parent tag and create a note of the child
### Adding new fields
- Create a note with the fileClass implemented

Method one
- Should see these buttons available now beside title
- Open the note -> 3 dots in the top right -> `Manage fields`
- There's a lot of customizability, but for the most part, you can just create your own selections
- Sometimes it will ask for a [[DataviewJS]] query (ex. links), which gives you the opportunity to dynamically choose what links are possible


Once you set up your fields, you can try it out on a note!
### Combining fileClass
Just create another note like `friend` and add both tags

You can also have tags inherit the fields of a parent tag, like how the `#i/book` tag inherits `#i` fields

### Editing Fields
- If you set up the fileClass, you will be able to see a new button beside the name of  the note in the:
	- tab
	- file explorer
	- link to the note
#### Editing in-table
You need to use DataviewJS tables to be able to modify the data while viewing the table.

You'll need to include the following code inside the table:
```js
const {fieldModifier: f} = this.app.plugins.plugins["metadata-menu"].api;
```

This provides a function that can be wrapped around a field in the table to allow for in-view editing.

Here's an example of a table to show all notes with a `#person` tag and it's fields
- `p` is the page

````
```dataviewjs
const {fieldModifier: f} = this.app.plugins.plugins["metadata-menu"].api;

console.log('pages,', dv.pages("#person"))

dv.table(["Name", "Age", "Email", "Phone"],
	dv.pages("#person")
	.filter(p => !p.file.path.includes('templates'))
	.filter(p => !p.file.path.includes('fileClass'))
	.map(p => [
		p.file.link,
		f(dv, p, "Email"),
		f(dv, p, "Phone")
	]));
```
````

```dataviewjs
const {fieldModifier: f} = this.app.plugins.plugins["metadata-menu"].api;

console.log('pages,', dv.pages("#person"))

dv.table(["Name", "Address", "Interests", "Friend?"],
	dv.pages("#person")
	.filter(p => !p.file.path.includes('templates'))
	.filter(p => !p.file.path.includes('fileClass'))
	.map(p => [
		p.file.link,
		f(dv, p, "address"),
		f(dv, p, "interests"),
		f(dv, p, "friend")
	]));
```
### View notes
*I would recommend removing filtering out `fileClass` and `templates` just in case like so*
````
```dataview
table address, interests, friend
from #person AND !"templates" AND !"fileClass"
```
````

```dataview
table address, interests, friend
from #person AND !"templates" AND !"fileClass"
```
### fileClass Menu View
There should be an icon beside the title of a fileClass note, which should open a view to manage that specific fileClass.
#### Table View
One of the options is "Table View", to which you can easily modify metadata and search for notes.
#### FileClass Fields
Another way to create fields
### Field Options
#### Suggest based on dataview query
- If you set a field to be a link, you can use a dataviewjs query to filter out options for the suggestion
- See [[projects]] for an example
#### "Will"Options
`Accept a link`
- Create a dataviewJS query to find all relevant notes based on dataview
#### Lookup Fields
> [Example](https://www.youtube.com/watch?v=ad0nJf8TZP8&ab_channel=MathieuDelobelle)
- Created a field called `boys`, which found all notes that had a `#student` tag with `gender` set to `male`

Automatic queries that are run whenever you create a new inline field in your notes.

Essentially, you can attach a dataviewJS query onto a field so as soon as you create it, it automatically prints something.

In his video example, he uses it to get the averages of days.

Wait. That'd actually be useful for weekly statistic averages.
Oh well, this plugin already has a lot, I'll update this another time.
___
References:

Created:: 2022-10-29 16:31