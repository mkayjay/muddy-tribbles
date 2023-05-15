Status:: 
Tags:: 
Links:: [[Obsidian MOC]] - [[Vault Features]]
___
# PARA Method in Obsidian MD
## Principles
- Read about the [[PARA Method]] note if you haven't already
### Why no folders!?
There are folders set up in this vault, but my preferred method is to utilize the linking capabilities of Obsidian 😎

Instead of having folders, you organize everything via links.

I just personally prefer to dynamically link notes rather than manually move them using hotkeys or via the file explorer.

It also allows notes to be in multiple places at once, and utilize the powers of plugins like [[Dataview Plugin]]

If you do want to use folders, you can leverage the tags in the templates to automatically move them upon note creation using [[Automatically move notes to a folder|Auto Note Mover Plugin]]
### Downsides
The abundance of connections may make it hard to differentiate between "Area" or "Resource" notes. I would counteract this by keeping the notes in my areas more personalized to my life that guide to actual resource notes or more personal stuff.

ex) For my personal brand, I would have a `My Personal Brand` note where I can include things I frequently visit like:
- More notes like `My YouTube Channel`, `My Sponsorships`
- A projects query for things related to the area
- A query for inputs that are linked to the note
- A resource note like `Copywriting MOC` or `Entrepreneurship MOC`

To my knowledge, there's no effective way to create a true archives page. A note may be linked to an area note, but since the note itself doesn't have the link, it would be considered an archived note. For now, it just includes notes in the folder.

If you want to hide archived notes in [[Dataview Plugin]] queries, you can add `AND !"4. Archives"` at the end of the `FROM` field
## Categories
### Projects
See [[Managing projects]] and [[Managing tasks via kanbans]]
### Areas and Resources
Each category has a `## Notes` heading for manual entries, while the `## All` heading uses Dataview queries to list out any respective notes
- Tag a note with `#area` or `#resource`
	- ex) [[Personal Knowledge Management MOC|PKM MOC]] is shown in `[[My Resources]]`  because it has the `#resource`
- ex) If I wanted to move it from `Resources` to `Areas`, I would change the link inside the note from `#resource` to `#area`
### Archives
![[Automatically move notes to a folder#^1ba03f]]

___
References:

Created:: 2022-07-07 00:52