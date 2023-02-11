---
alias: Church Health
type: MAP
subject: 
description: 
tags: 
banner: "![[Fog Church.jpg]]"
banner_y: 2
---
# Church Health MAP
>[!verse]+ 1 Peter 5:2
> ![[1 Pet-05#v2]]

```spotlight-note
match=3 Archives/People
divAlign=left
```

>[!multi-column]



## Newest Contacts
```dataview
TABLE without ID
file.link AS "Name", membership AS "Member", baptized AS "Baptized", round(dur(date(today) - birthday).years, 0) AS "Age" 
FROM "3 Archives"
WHERE
type = "person"
SORT
file.ctime DESC
LIMIT 10
```

## Small Groups
```dataview
TABLE without ID
	file.link AS "Small Group ID", sgLeaders AS "Leaders", sgMembers AS "Members"
FROM "3 Archives"
WHERE type = "smallGroup"
```