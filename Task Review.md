> [!done]  Checked:
> [[2022-10-29 Saturday]]
> [[2022-11-05 Saturday]]

# Tasks not yet assigned (CW45) 
```dataview 
TASK WHERE !completed 
AND contains(tags, "task") 
AND !contains(text, "CW45")
SORT tags ASC
GROUP BY file.folder
```
# All Tasks
```dataview 
TASK WHERE !completed 
AND contains(tags, "task") 
SORT tags ASC
GROUP BY file.folder
```

# Additional  Items
## Actionable Ideas
```dataview 
TASK WHERE !completed AND contains(tags, "#idea")
GROUP BY file.name
```


## To Read
```dataview 
TASK WHERE !completed AND contains(tags, "#toread")
GROUP BY file.name
```
```query 
tag:#idea
```

## Delegated
```dataview 
TASK WHERE !completed AND contains(tags, "#delegated")
GROUP BY file.name
```

## Reminder
```query 
tag:#reminder
```