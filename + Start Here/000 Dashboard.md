---
type: index
tags: Example
---
# Home

> [!tip]-  Upcoming Teachings
> ```dataview
> TABLE without ID
> 	file.link AS "Lesson",
> 	type AS "Type",
> 	date,
> 	description AS "Description",
> 	topic AS "Topic",
> 	series AS "Series",
> 	teacher AS "Teacher",
> 	themes AS "Themes",
> 	file.etags AS "Tags"
> FROM "1 Lessons"
> WHERE
> 	contains(type,"Teaching")
> SORT
> 	date
> ```

>[!verse]- Most Recent Personal Study Notes
> ```dataview
> TABLE without ID
> 	file.link AS "Note", 
> 	file.path AS "File Path",
> 	passage AS "Passage",
> 	majorTheme AS "Major Theme",
> 	date AS "Last Edited"
> FROM 
> 	"3 Archives" 
> WHERE
> 	type = "personalNote"
> LIMIT 15
> SORT
> 	file.mtime DESC
> ```


>[!map]- MAPS
> ```dataview
> LIST WITHOUT ID
> 	link(file.link, alias)
> FROM 
> 	"2 Maps"
> SORT
> 	file.name ASC
> ```

>[!book]- Articles
> ```dataview
> TABLE  without ID
> 	file.link AS "Title", 
> 	source as "Source",
> 	author as "Author",
> 	description as "Decription"
> FROM 
> 	"3 Archives"
> WHERE
> 	type = "article"
> SORT
> 	file.mtime DESC
> ```
> 

