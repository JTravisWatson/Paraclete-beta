---
type: index
banner: "![[Bookshelf.webp]]"
banner_x: 0.5
cssClass: three-column-list
---
# Home
%% ![[Buttons#^button-new-sg]] %%

## Upcoming Lessons and Sermons
```dataview
TABLE without ID
	file.link AS "Lesson",
	type AS "Type",
	date,
	description AS "Description",
	topic AS "Topic",
	series AS "Series",
	teacher AS "Teacher",
	themes AS "Themes",
	file.etags AS "Tags"
FROM "1 Lessons"
WHERE
	type = "sermon" OR type = "lesson"
SORT
	date
```

## Most Recent Personal Study Notes
```dataview
TABLE without ID
	file.link AS "Note", 
	location AS "location",
	passage AS "Passage",
	majorTheme AS "Major Theme",
	date AS "Last Edited"
FROM "3 Archives"  
WHERE
	type = "personalNote"
LIMIT 15
SORT
file.mtime DESC
```


## MAPS
```dataview
LIST WITHOUT ID
	link(file.link, alias)
FROM "2 Maps"
SORT
	file.name ASC
```

## Articles
```dataview
TABLE  without ID
	file.link AS "Title", 
	source as "Source",
	author as "Author",
	description as "Decription"
FROM "3 Archives"
WHERE
type = "article"
SORT
file.mtime DESC
```

## Table
```dataview
LIST WITHOUT ID
	link(file.link, alias)
FROM "2 Maps"
```




> [!timeline]+ Title
> Contents
