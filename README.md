# Obsidian-GTD-Templates ( In draft )
My GTD Templates and views. 
This aproach is trying to address Note based priority based on folder levels and tasks. 

- New notes will be added on Inbox. 
- Actionable notes will be on 1X folders. 
For example: 
**Contexts** - Based on tags. Eg.: #Area/AreaName
On the context I have a file as below:
 
- Active projects folder - Project on focus 
- Next - Actionable notes 
- Later ( Intermediate level between Next and Someday ) Not mandatory and not official on GTD. But it helps to organize
- Someday 

- Completed notes should be moved to 99 - Completed

## Focus ( Top 3 )

```dataview
LIST
FROM #Area/AreaName   
WHERE contains(file.folder,"Project") 
sort file.folder
limit 3
```

## Planning

```dataview
TABLE without id
file.link as "Project",
file.folder as "Folder"
FROM #Area/AreaName   
WHERE contains(file.folder,"Next") or  contains(file.folder,"Someday") or contains(file.folder,"Project")  or contains(file.folder,"Later")
sort file.folder
```


## Required plugins
The Obsidian setup requires the plugins below:
### Obsidian taks - https://github.com/obsidian-tasks-group/obsidian-tasks
Provide a task functionality. On plugin configuration panel, enable "Set done date on every completed task", 
"Auto-suggest task content" and "Provide access keys in dialogs".


### Obsidian Dataview - https://github.com/blacksmithgu/obsidian-dataview
### Obsidian Calendar - https://github.com/liamcain/obsidian-calendar-plugin

## Nice to have
### Obsidian Outliner -  https://github.com/vslinko/obsidian-outliner
- Help to move tasks and bullets to up and down
### Obsidian templater - https://github.com/SilentVoid13/Templater
- Help to automate daily templates

## Folders
Folders use a number prefix to sort them on side panel. 

![imagem](https://user-images.githubusercontent.com/4821589/206133551-3a597c08-9ce2-4418-9ff8-32f33eeb0a92.png)


- /00 - Inbox 
- /01 - Journal
- /02 - Views 
- /10 - Contexts 
- /11 - Acrive Projects
- /12 - Next
- /14 - Later 
- /15 - Someday
- /90 - Reference
  - Archived projects
  - Companies
  - Files
  - Notes
  - People
  - Templates
/99 - Completed 

![imagem](https://user-images.githubusercontent.com/4821589/206133667-85f2e9d2-7d5b-4ed4-bdd1-d4c51e61d000.png)


## Views
View folder has dataview widgets to help you to manage notes and tasks

![imagem](https://user-images.githubusercontent.com/4821589/206135530-bff5920a-788b-48e1-8c6b-92e5148b3487.png)


Reach me if you find this useful. 

