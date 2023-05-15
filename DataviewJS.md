Status:: 
Tags:: 
Links:: [[Dataview Plugin]]
___
# DataviewJS
## Principles
Integrates JavaScript operations to create dataview queries 🤯

It might be a bit complex to learn in the beginning, but it's worth it, as it lets you create in-table-editable fields in dataview queries when paired with the [[Metadata Menu Community Plugin]]
### Resources
- [Intro documentation page](https://blacksmithgu.github.io/obsidian-dataview/queries/dql-js-inline/)
- [DataviewJS Snippet Showcase](https://forum.obsidian.md/t/dataviewjs-snippet-showcase/17847)
### Code Examples
#### View all projects with editable column values
````
```dataviewjs
const {fieldModifier: f} = this.app.plugins.plugins["metadata-menu"].api;

console.log('pages,', dv.pages("#🚧"))

dv.table(["Name", "Deadline", "Area"],
	dv.pages("#🚧")
	.filter(p => !p.file.path.includes('templates'))
	.filter(p => !p.file.path.includes('fileClass'))
	.map(p => [
		p.file.link,
		f(dv, p, "Deadline"),
		f(dv, p, "Area")
	]));
```
````
___
References:

Created:: 2022-10-30 17:19