#GTD
```dataview
TASK FROM "" 
WHERE contains(text, "#WaitingFor") and 
!completed
Group by due
```