Status:: 
Tags:: 
Links:: [[_start_here]]
___
# Troubleshooting
## General
### How do I add notes from other places
- Text-based files should be in markdown

### I already have a vault
- What I found to work was just copying all relevant files into my own vault
- All the search query notes
- Templates
- `.obsidian/plugins/x` where x are the required plugins
## User Interface
### Plugins are inactive or missing in the sidebars
- If they say something like "plugin x not found"
- Seems to happen upon a fresh open after downloading
- Go to settings and make sure they're all enabled, then go quit and re-open the app
### I don't see buttons or queries
- ![[Vault Overview#^531cbd]]
## Workflows 
### Tasks don't show up in daily note
In the code block there's the following line:
```
from [[<%tp.file.title%>]]
where kanban-plugin = "basic"
```
if you remove the `from [[<%tp.file.title%>]]` and replace it with `from ""` it may help, but I found that if you have a lot of notes like me it will make the vault lag since you're looking through every note for tasks instead of only ones that are linked to the same date
### Dates are not properly set

- This is most likely a timezone issue, which I sacrificed in order to let the templates work no matter what time you create them

	- If you find yourself having issues, replace all instances into the format `<%tp.date.now('YYYY-MM-DD')%>` (current day of creation) or it's equivalent
		- `<%tp.date.now('YYYY-MM-DD', -1)%>` would be yesterday
		- `[[<%tp.date.now("YYYY-[W]ww", -9)%>]] <== This Week ==> [[<%tp.date.now("YYYY-[W]ww", 2)%>]]` would be for if you were to create the weekly note on a Sunday and wanted to link it to last/previous week
		- Just keep experimenting until the dates and links are accurate, and message me if you need help !
### Dates are incorrect in periodic reviews
For example, in the daily note the links to previous/future days are off, or the week is off, or the query to view tasks on the current day is off

Make sure that when you CREATE the note using QuickAdd, it follows the following formats: ^ch4g25
- `2022-W28` for weekly
- `2022-M08` for monthly
- `2022-Q3` for quarterly
- `2022` for yearly

This helps template properly retrieve the date from the title to generate the required links to other notes and automatically set up ranges for tracking charts, queries, etc
- ex) `<% moment(tp.file.title,'YYYY-MM-DD').add(-1,'days').format("YYYY-MM-DD") %>` bases the output on the title of the note rather than the actual date, so even if you created the `2022-07-21` note on `2022-07-19` it would still work

If you're not from North America, then the way the automatic date templates are 
I'm not 100% sure how to fix it, but what you can do is just do a little bit of experimenting to see the correct template command that works best for you.
Right now I use the file name to determine the kind of links it should have, with an example being using a weekly note's title to determine the previous weekly note:
`<% moment(tp.file.title,'YYYY-[W]WW').format("YYYY") %>-W<% moment(tp.file.title, "YYYY-[W]WW").add(-2, 'weeks').week() %>`
- `moment()` is what turns the title of the note and explains how the date is being formatted (the square brackets tell it to simply output whatever is inside since normally certain letters are used to reference format as seen in YYYY as the year)
- `.format()` then applies your chosen formatting, which you can learn more about https://devhints.io/moment

There are two options:
1. You can use a different way to generate the links based on the time you created it, but that requires you to create the note on the correct date so the code works as intended
	- I previously used to use something along the lines of `<%tp.date.now("YYYY-[W]ww", -2)%>` where I would just keep testing different numbers (which in this case are the difference in days) until the link generated would be on the previous week
2. You can just play around with the first number in `.add()` until it works, and you can also try changing it to `days` instead of `weeks`
	- When trying to find the first day of the week like in the key metrics chart, the number in `.day() correlates the numbers 0-6 to a day in the week` 
### Templates are not working in mobile
- When I tried it out, for some reason my templates folder became capialized on mobile which made plugins like templater and quickadd not recognize the templates. To circumvent this you can create a duplicate folder of your templates (which is tedious) until a better solution is found :/
___
References:

Created:: 2022-07-10 23:37