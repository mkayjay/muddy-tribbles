Status::
Tags:: 
Links:: [[Template Debrief]]
___
# Template Explanations
## Inputs
### Input Template
Pretty self-explanatory, refer to [[My Inputs Workflow]]
### Book Template
Learn how to use the book templates [here](https://www.youtube.com/watch?v=z2NW1iVlkp8&ab_channel=JohnMavrick) and an example of me taking notes and my thought process [here](https://www.youtube.com/watch?v=WlwyYwP3HLg)
## Periodic
### Daily Note Template
- See [[2022-07-09]] for example use
#### Metadata
- Used for the weekly overview
- Can create your own to display in dataview queries
	- [[Metadata]]
#### Today
- Queries for any kanban tasks/cards due for the day, inspired by [this](https://forum.obsidian.md/t/kanban-plugin-and-dataview/36660/13)
- A log for any journalling you want to do about the day's events
	- Imports the [[Dailies]] note which includes your daily tasks/habits
		- Can use if statements to conditionally render certain tasks, like how I do with work and weekly reviews
#### Reminders
- The red `Today's Focus` block is a [[Obsidian Callouts]], so to put content inside of it just click on it and make sure the line is prefixed with `> `
#### Journals
- Whatever you want to write about, I personally just like gratitude and [High Performance Habit's Morning Mindset](https://www.highperformanceplanner.com/)
#### Reflection
- Metadata to add
	- Energies keeps track of my different kinds of energy, from 1-10
### Weekly Note Template
> [!INFO] 
> The template is created with the assumption that you do your weekly reviews on Sunday
> See [[2022-W28]] for example uses

#### [[Weekly Review Template#Future Plan|Future Plan]]
- `### Action items` will look for all the tasks `- [ ]` in the note for easy recollection after your reflection
##### Projects
- Query lists out all projects for the next week
	- Must have a link from the project note to the weekly note
#### [[Weekly Review Template#Recap|Recap]]
`### Days`
- Query to show the days, and its related metadata in [[Daily Template#Reflection]]
	- Rating is what you set in the [[Metadata]] of the note
	- ✍️ are the different headers (Content Log, Gratitude) I linked to just to make it easy to have an overview of the week's content
		- Use the preview feature by hovering over the emoji to quickly see what was inside
- `### Key metrics` can be used to keep track of measurables like hours slept, pages read, etc
	- In this case, I just have it set to my energy level recordings from each day
	- To create your own, just follow the structure of the code snippet, and follow [[Daily Template#Energies|the double colon stuff]]
	- Uses the Obsidian tracker plugin to visualize metadata
		- Charts will only render if all the daily notes in the range are created
- `### Projects` query displays all projects you did this week (must be linked to the weekly note)
#### [[Weekly Review Template#Reflection|Reflection]]
- Include whatever prompts you want to inspire retrospection, I personally use the content from [High Performance Habits Weekly Planner](https://www.highperformanceplanner.com/) (learning review, life review) and my own prompts
	- Whenever you want to keep track of something, just add a checkbox prefix `- [ ]` and it will be added to the `Action Items` query
### Periodic (Monthly, Quarterly, Yearly) Notes
- All have a similar structure modified in respect to the timeframe
- Instead of having to change the same section in each review note, I make them all import the related note like [[Focus Area Addon]] so I only have to make the changes once via <%tp.file.include("`[[note]]`")%>
`### Focus Areas`
- Areas in your life you want to focus on, can be related to [[⛰️ My Areas]] 
- Break down your focus into smaller projects for the following weeks
`## Reflection`
- More generic and higher-order prompts to reflect on the timeframes as a whole, as more intricate reflection is done in the weekly reviews
#### Monthly Note Specific
- Contains a month-long view on whatever statistics you decided to track (ex. energies)
## Note Types
### Note Template
Self-explanatory, just remember [[Template Debrief#What do I put for status tags and links|what to put for status tags and links]]
### MOC Template
#### Queries
Backlinks to more connected notes become congested, so I created queries to separate the kinds of notes it connects to
## Productivity
### Project Template
- Random `<% ... %>` is to move the note to a projects folder with the name as the note title
- Remember to link the project to it's respective weeks to be shown in [[Weekly Review Template]] queries
#### Kanbans
- See [[Kanban Board]]
#### Resources
- I'm not sure how you would add context for queries, so just make a manual link if you need to keep note of something
#### Planning
- Based on the [[Objective Key Results (OKR)]] model
### Kanban Template
If the kanban view doesn't load, click on the 3 dots in the top right to change the view
## Addons
Add into where your cursor is via `Ctrl+Shift+T`
### Progressive Summarization Checklist
Just a mini-checklist to include in your input notes for [[Progressive Summarization]]
___
References:

Created:: 2022-07-07 22:34