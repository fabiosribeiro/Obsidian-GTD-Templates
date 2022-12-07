
## Projetos sem Contexto
```dataview
TABLE without id
file.link as "Project"
FROM "11 - Active Projects" or "12 - Next" or "14 - Later" or "15 - Someday"
WHERE !contains(file.tags, "#Area") and !contains(file.tags, "#Work") 
```

