---
alias: Atlas
status: 
type:
description: A Map of all of the Maps.
tags: 
---
# The Atlas
This page hosts the descriptions and links to all of the major portions of the vault.

```dataview
LIST
	rows.customValue
FROM
	"2 Maps"
WHERE
	contains(type,"MAP")
FLATTEN 
	link(file.link, alias) + "-> " + description AS customValue
```


## Study
>[!blue]+ Resources for personal study
> 



## Prepare
>[!orange]+ Lesson and Sermon Prep
>


## Connect
>[!green]+ Resources for shepherding your flock
>