[[Barack Obama]]

```dataview
table address, interests, friend
from #person AND !"fileClass" AND !"templates"
```


```dataviewjs
const {fieldModifier: f} = this.app.plugins.plugins["metadata-menu"].api;

dv.table(['Name', 'Address', 'Interests', 'Friend'],
	dv.pages("#person")
	.filter(p => !p.file.path.includes('templates'))
	.filter(p => !p.file.path.includes('fileClass'))
	.map(p => [
		p.file.link,
		f(dv, p, "address"),
		f(dv, p, "interests"),
		f(dv, p, "friend")
	])
)
```
