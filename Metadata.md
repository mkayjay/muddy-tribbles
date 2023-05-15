Status:: 
Tags:: 
Links:: [[Obsidian MOC]]
___
# Metadata
## Principles
Information about the note that can be viewed in dataview queries

### Adding Metadata

You can add it at the top of a note. If I wanted to add the data `hoursSlept` with a value of 8, I would add this at the top of my note:
```md
---
hoursSlept: 8
---
```
This is known as frontmatter.

Another way to do it is to have it inline in the text, with two colons after the name
- An example is the `Created` line below where it turns the date it was created into a variable viewable by queries
### Types
- Can be your average variable types found in programming languages like numbers, strings, and booleans
- Can also use YAML language to add nested lines like found in the [[Daily Template]] frontmatter metadata
### Uses
- Can view this data in [[Dataview Plugin|Dataview queries]]
___
References:

Created:: 2022-07-14 00:15