Status::
Tags:: #plugin
Links:: [[Obsidian Community Plugins]]
___
# Dataview Plugin
> [Easy to use dataview query builder](https://s-blu.github.io/basic-dataview-query-builder/)
> [Official Docs](https://blacksmithgu.github.io/obsidian-dataview/docs/intro)
## Principles
- If you want to better understand how it works, check out how I use queries to sort my school notes [here](https://youtu.be/0UTzpIdLbVo?t=98)
- Queries notes based on its characteristics
	- What folder it's in, if it's linked to a certain note, what tags it has, its metadata, etc
- Allows to display the note's metadata as columns in a table
- The use cases for this include
	- categorizing notes like in [[📥 My Inputs#Inputs Sorted]] based on completion, while also showing its started/finished dates
	- finding notes that connect to the already existing note (queries in the MOC template or 200 Areas/300 Resources)
### Fields
````
```dataview

TABLE|LIST|TASK <field> [AS "Column Name"], <field>, ..., <field>

FROM <source> (like #tag or "folder")

WHERE <expression> (like 'field = value')

SORT <expression> [ASC/DESC] (like 'field ASC')

... other data commands

````
#### DISPLAY
- The kind of view you want
	- Table includes metadata displayed as column
	- List is just the file name
	- Task is for the todo's in a file I think?
#### FROM
- `[[]]` will refer to the note the query is in
- Dictates the files you want to consider
- `[[fileName]]` will include files that link to `fileName`
- `outgoing([[fileName]])` includes the outgoing links from inside `fileName`
#### WHERE
- `where contains(lower(file.name), "string")` will include all files that include the text `string`, regardless of casing due to `lower()`
- `where file.name[x]` will include all files where the xth char (starting from 0) is equal to whatever expression you do
## Examples
Check almost any [[Template Explanations]] ;)
#### Files that link to this file that aren't outgoing links (run the "replace templates" command for it to activate)
```dataview
list
from [[]] and !outgoing([[]])
```
___
References:

Created:: 2022-07-07 21:11