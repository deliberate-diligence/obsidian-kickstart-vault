# Notes
```dataview
TABLE file.cday as "File" 
WHERE contains(reviewed, "no")
	AND file.folder != "Templates"
SORT file.ctime
```
# Daily Concerns
```dataview 
TASK WHERE !completed 
AND contains(meta(section).subpath, "Concerns")
GROUP BY file.name
```

