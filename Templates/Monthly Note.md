---
reviewed: no
---
# Masterplan & Success Log
```dataview 
TASK 
WHERE header = [[2022-Q4#2022-10 October]]
```

# Monthly Routine
- [ ] Review the month's note and setup the following month's note
	- [ ] Fill out Success Log
	- [ ] Fill out Masterplan
- [ ] Do a Kanban Braindump
- [ ] Explore tags for thought and inspiration

# Tasks
## To do
```dataview 
TASK WHERE !completed
AND file.ctime.year = 2022
AND file.ctime.month = 9
AND contains(tags, "#task")
GROUP BY file.cday
SORT tags ASC
```

## Done
```dataview 
TASK WHERE completed
AND file.ctime.year = 2022
AND file.ctime.month = 9
AND contains(tags, "#task")
GROUP BY file.cday
SORT tags ASC
```


# This Month's Notes
```dataview 
LIST file.cday
WHERE file.ctime.year = 2022
AND file.ctime.month = 9
SORT file.ctime ASC
```