---
reviewed: no
---
# Masterplan & Success Log
```dataview 
TASK 
WHERE header = [[2022-Q4#2022-CW44]]
```

# Weekly Routine
- [ ] Work Email Inbox Zero
- [ ] Finance Updates
- [ ] Review Week/Month/Quarter/Year
	- [ ] Do a Braindump into Week, Month, Quarter, and Year; check items for relevance
	- [ ] Select Tasks for next week
	- [ ] Check next week's calendar for surprises and block out rest times
	- [ ] Check "To Review" note
	- [ ] Write down successes for last week's note
- [ ] Do your regular backups
- [ ] Clean appartements
- [ ] Water Plants
- [ ] Readwise sync

# Tasks

## Essential Few
```dataview 
TASK WHERE !completed
AND (contains(tags, "p1") OR contains(tags, "now"))
SORT tags
```

## Unessential Many
```dataview 
TASK 
WHERE !completed 
	AND contains(text, this.file.name)
	AND !contains(tags, "p1")
	AND !contains(tags, "now")
SORT tags
GROUP BY file.cday
```

## Done
```dataview 
TASK WHERE completed AND contains(text, this.file.name)
SORT tags
```

# This Week's Notes
```dataview 
TABLE file.ctime as "Created"
WHERE file.ctime.weekyear = this.file.cday
SORT file.ctime ASC
```