---
alias: Teachings
status: 
type: MAP
description: A MAP of all Lessons and Sermons.
tags: 
banner: "![[Congregation Bible.jpg]]"
banner_y: 0.6
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
FROM "1 Lsssons" OR "3 Archives"
WHERE
	type = "lesson" AND status !="idea"
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
FROM "1 Lsssons" OR "3 Archives"
WHERE
	type = "sermon" AND status !="idea"
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


