#GTD

## 🎯 Goals in focus

```dataview
TABLE without id
file.link as "Goal",
file.folder as "Status"
FROM #Goal  
WHERE contains(file.folder,"Active Projects")
sort file.folder
```

## ⛳ Focus
```dataview
TABLE without id
file.link as "Project"
FROM "11 - Active Projects" or #Focus
WHERE !startswith(file.path,"90 - Reference/Templates")
```

## ⌛ Delayed
```tasks
not done
happens before today
sort by path, priority, due reverse
group by filename
```

## 🚩 Important

``` tasks
not done
priority is high
happens before tomorrow
sort by path,due,priority
```

## 📢 Medium Prio
``` tasks
not done
priority is medium
happens today
sort by path, description, priority
```

## 📢 Low Prio
``` tasks
not done
priority is below medium
happens today
sort by path, description, priority
```


## 🗼 Tomorrow
``` tasks
not done
happens tomorrow
sort by path, description, priority
```

## 🎗️ Next days
``` tasks
not done
priority is above none
happens after tomorrow
sort by due, priority
limit 10
```

## ✋ Waiting For

```dataview
TASK FROM "" 
WHERE contains(text, "#WaitingFor") and 
!completed
Group by file.path
```


## 📖 Reading list
```dataview
TASK
FROM ""
WHERE contains(tags, "#readIt") and 
!completed
```

## ⚠️ Important - No due date
```tasks
not done
priority is high
no due date
no start date
limit 10

```

## ✔️ Done
```tasks
done today
```
