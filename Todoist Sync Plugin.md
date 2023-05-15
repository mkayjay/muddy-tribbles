Status: 
Tags: 
Links: [[My Plugins]]
___
# Todoist Sync Plugin
> See why I recommend you use it in [[Managing tasks via Todoist]]
## Principles
### Resources
Read more about how to use it in the [Github](https://github.com/jamiebrynes7/obsidian-todoist-plugin) page

To create custom queries, learn about Todoist's [filters](https://get.todoist.help/hc/en-us/articles/205248842-Filters) you can include in the `filters` field

If you want some more Todoist integration, you can search up "Todoist" in community plugins for plugins that instead turn tasks into markdown checkboxes, or have two-way linked syncing.

Video soon!
### Query Parameters
All the common options you can use can be found in the below query
- `group` groups the tasks by section when being displayed (see [[#View all due today's tasks sorted by date then priority]])
- `&` to require both expressions to be true, `|` for at least one
- `()` to make the inside expressions evaluate first
- Only end the line with a `,` if it's not the last one
- Change placeholder things like `Header Name` , `Project` and `Section` into their actual counterparts :p
````
```todoist
{
	"name": "Header Name",
	"filter": "(overdue | today | no due date) & #Project | /Section & @label",
	"sorting": ["date", "priority"],
	"group": true
}
```
````
### Tips
- If grouping by section, you can click on it to hide it
## Examples
Feel free to go into preview mode and copy the code block!

It's recommended that you have Todoist sync enabled and set up with some tasks populated so you can see the examples work.

Since the queries are based on the current date, if you were to visit a past daily/weekly note, it would show the same results as one in the current weekly note.
### View all due/today's tasks sorted by date, then priority

The following should be copy-pasteable:
````
```todoist
{
"name": "For Today",
"filter": "(overdue | today)",
"sorting": ["date", "priority"]
}
```
````
- `filter` includes only tasks that are overdue or are due today
- `sorting` first sorts by date to put due tasks in front, then sorts those groups by priority
#### Example
```todoist
{
"name": "For Today",
"filter": "(overdue | today)",
"sorting": ["date", "priority"],
}
```
### This Week
If your week starts on a Monday (if not, just change it to when you start your week).

The following should be copy-pasteable:
````
```todoist
{
"name": "This week's tasks (including Sunday)",
"filter": "due before: mon",
"sorting": ["date", "priority"],
"group": true
}
```
````
- `group` helps organize it into the different projects you have going on, but can be removed
#### Example
```todoist
{
"name": "This week's tasks (including Sunday)",
"filter": "due before: mon",
"sorting": ["date", "priority"],
"group": true
}
```
### Next Week
Should be copy-pasteable:
````
```todoist
{
	"name": "This week's tasks (including Sunday)",
	"filter": "due after:sun & due before:next mon",
	"sorting": ["date", "priority"],
	"group": true
}
```
````
#### Example
```todoist
{
	"name": "Next week's tasks",
	"filter": "due after:sun & due before:next mon",
	"sorting": ["date", "priority"],
	"group": true
}
```
### Project
**Since each project and section tag will be different for each project note, you will have to set it up in Todoist and fill it out in the [[Project Template]] each time.**

I would personally turn The `## Kanbans` header into something like `## Tasks`, and then have `Kanbans` and `Todoist` as subheaders.

Here's an example skeleton you can add for it, where you need to populate the `#` and `/` (feel free to add [[Template Debrief#tp file cursor|cursor checkpoints]])

````
```todoist
{
"name": "Todoist",
"filter": "# & /",
"sorting": ["date", "priority"]
}
```
````

For a project named `misc` and a section named `periodicReviews`

````
```todoist
{
"name": "Periodic Reviews",
"filter": "#misc & /periodicReviews",
"sorting": ["date", "priority"]
}
```
````
#### Example
```todoist
{
"name": "Periodic Reviews",
"filter": "#misc & /periodicReviews",
"sorting": ["date", "priority"]
}
```

___
Created:: 2021-09-11 13:14
