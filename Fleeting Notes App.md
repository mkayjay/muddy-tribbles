Status:: 
Tags:: 
Links:: [[Fleeting Notes]]
___
# Fleeting Notes App
*Disclaimer: I am a co-founder of the app, but it is 100% free to use and I genuinely do think it helps solve the problem of quick capture, or else I wouldn't be doing this ;)*
## Principles
[Fleeting Notes](https://fleetingnotes.app/) is Google Keep but tailored with the Obsidian and Zettelkasten experience in mind.

You can start trying it [here](https://my.fleetingnotes.app/)
### Setup Process
To retrieve your notes from Fleeting Notes, follow the [guide here](https://fleetingnotes.app/posts/sync-fleeting-notes-with-obsidian/) to set up your Fleeting Notes account
## Workflows
### Capturing
#### Quick Capturing Ideas
- When I'm on a walk, I can easily take out my phone, open the app, and turn on my keyboard's voice to text feature to start word vomitting whatever's on my mind
#### Web Clipper
- You can enable a setting in the app to automatically save the URL of notes when using it on the web
- When highlighting something, just right click, and then choose the Fleeting Notes option
- It also saves things like video timestamps
#### Standalone App
You can open a pop-out window by right clicking on your browser, or pin the chrome/firefox extension on your toolbar
### Processing
#### Syncing
- After setting up your credentials in the community plugin, you can run the command `Sync Notes with Fleeting Notes` to import all your notes
	- Alternatively, you can also modify your syncing style to delete notes on FN after syncing, or to enable two-way sync
	- You can customize the way they are imported to your liking using the customizable import template
		- Either let it imitate your existing default Note Template, or keep it as a mere fleeting note that is temporary
##### Templates
`${datetime}` is a long timestamp including seconds
`${created_date}` and `${last_modified_date}` is formatted in `YYYY-MM-DD`

Using it as temporary content:
```
---
# Metadata used for sync
id: "${id}"
title: "${title}"
created: "${datetime}"
source: "${source}"
tags: "#note/🌱"
---
${content}
```

Using it as permanent-note-ready:
```
---
# Metadata used for sync
id: "${id}"
title: "${title}"
created: "${datetime}"
source: "${source}"
---
Status:: #note/🌱 
Tags:: 
Links:: 
___
# <%tp.file.title%>
${content}
___
Created:: ${created_date}

```

#### Finding Notes
[Watch example workflows](https://www.youtube.com/watch?v=iXLyEvTZp9I&ab_channel=MatthewWong)

##### Finding notes
- Fleeting Notes will go to the `FleetingNotesFolder`, which you  can change in the settings
- In the case of this vault, you can find all of them as seedling notes in [[🌞 My Greenhouse]]

Inserting Notes
- You can run commands like `Insert Unprocessed Notes` or `Insert All Notes that Contain Specific Text`
___
References:

Created:: 2022-09-05 11:41