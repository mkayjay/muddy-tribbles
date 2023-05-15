Tags:: #🔍
Links:: [[🏠 My Home]] - [[🚧 My Projects]]
___
# 📌My Kanbans

> [!WARNING] Missing tasks?
> *Sometimes the `#kanbans ` tag disappears in the [[Kanban Template]], which may prevent it from loading here or in the daily notes*.
> To solve this, check [[Vault Troubleshooting#Tasks don't show up in daily note]]

See [[Managing tasks via kanbans]] for how to use!

```button
name Create Kanban
type command
action QuickAdd: 📌 Create Kanban + Set Folder
```
## All
```dataview
table file.mtime as "Last Modified"
from #kanbans AND !"templates"
sort file.mtime desc
```
___