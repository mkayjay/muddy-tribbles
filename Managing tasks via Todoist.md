Status:: 
Tags:: 
Links:: [[Vault Features]]
___
# Managing tasks via Todoist

> [!INFO] Video Alternative
> Watch my [Ultimate Task Management video](https://www.youtube.com/watch?v=t_nX51ODmPU) to see how I set up Obsidian and Todoist

I decided not to have it implemented in case people use other apps for task management, but this page will contain everything you need to set it up.
## Why not native task management?

- Kanbans are better for tracking status than they are for general task management
- Quick capturing tasks for projects without using the daily note is frictionful
- Why not use an app that specializes in task management instead?
### Why use Todoist?
- Has plugins to see tasks in Obsidian like [[Todoist Sync Plugin]]
- I've personally used it on and off, but its ability to quick capture is second-to-none
- I just really enjoy todoist because of how fast you can create tasks
	- When setting up characteristics, you can just type something like `Task name today p1 #project/section` and it will automatically set the fields of the task
## Principles
### Setup
Create a [Todoist account](https://todoist.com/auth/signup) if you haven't already

Enable [[Todoist Sync Plugin]]

Obsidian settings > under community plugins sidebar header find "Todoist Plugin" settings page and put in your Todoist API token
#### Todoist App
Todoist categorizes tasks into two layers: projects > sections

Projects can be areas in your vault like [[⛰️ My Second Brain]] and sections can be projects like [[🚧 Vault Onboarding]]

Since I use the free version, I can only have 5 projects, so I have projects as my BROAD life areas (content creation, brand, [[Fleeting Notes App]]), and then categorize them into my more niche areas (Content > YouTube channel, Brand > Ultimate Starter Vault, etc)

If you need an extra layer, you can most likely use labels for it and just have your `filters` search be something like `#project & /section & @label`, or just pay for their premium plan 😅
### Creating Tasks
Download todoist or just use the built-in [[Todoist Sync Plugin]] commands (Search up `Todoist Plugin` in command pallete)
### Viewing Completed Tasks
*Completed tasks cannot be queried using the plugin, but you can fetch them using [Todoist Completed Tasks](https://github.com/Ledaryy/obsidian-todoist-completed-tasks)*

This means that you can't look back at previous weeks and see the tasks you had due on that week or in the next week.
___
References:

Created:: 2022-09-22 23:30