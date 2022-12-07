#GTD 

### Recently closed

```dataview
TABLE 
dateformat(file.mtime, "dd.MM.yyyy - HH:mm") AS "Changed date"
from "99 - Completed"

SORT file.mtime desc
limit 10
```



### Tasks recently done
- Limit: 200 tasks

```tasks
done
group by done
sort by done reverse
limit 250
```

