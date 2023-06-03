---
alias: Teachings
origin: 
type: MAP
description: A MAP of all Lessons and Sermons.
tags: 
---
# Lessons and Sermons MAP

> [!verse] 2 Timothy 2:2
> ![[2 Tim-02#v2]]


## Lessons
```dataview
TABLE without ID
	file.link AS "Lesson",
	description AS "Description",
	topic AS "Topic",
	series AS "Series",
	teacher AS "Teacher",
	themes AS "Themes"
FROM "1 Lessons" OR "3 Archives"
WHERE
	contains(type,"Lesson")
SORT
	date
```
## Sermons
```dataview
TABLE without ID
	file.link AS "Sermon",
	description AS "Description",
	topic AS "Topic",
	series AS "Series",
	teacher AS "Teacher",
	themes AS "Themes"
FROM "1 Lessons" OR "3 Archives"
WHERE
	contains(type,"Sermon") AND status !="idea"
SORT
	date
```
## Other presentations
```dataview
TABLE without ID
	file.link AS "Presentation",
	type AS "Type",
	description AS "Description",
	topic AS "Topic",
	teacher AS "Teacher"
FROM "1 Lsssons" OR "3 Archives"
WHERE
	type = "communion" OR type = "prayer meeting" AND status !="idea"
SORT
	date
```


