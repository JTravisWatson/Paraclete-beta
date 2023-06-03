
# Metadata Standards
This page contains the different variables, and their possible values, along with descriptions.

## Front Matter
All frontmatter should aim to be concise and descriptive.

### Universal Front matter
Some metadata values will appear in *all* file types.

```yaml
---
alias: 
origin: 
type: 
---
```

#### Definitions
- `alias` 
	- These are alternate, or simply more convenient names. The benefit of an `alias` is for easy search as well as another name to reference in a tag or link.
- `origin` 
	- This is the original author of the note. This variable is intended for attribution when notes are shared. You can either use your name, or a user name. However you want the community to identify you.
- `type` 
	-  This indicates what sort of note the document is, and is used for populating dynamic lists and tables. The Paraclete System uses a fixed set of values to define the types of notes in your vault. These are referenced in various `dataview` queries. Since each metadata variable can have multiple values, you can still use any other naming convention you want *alongside* the Paraclete naming.
		- `Teaching` 
			- This value is used for all teaching types. These are specifically for teaching that you *give*, not teachings you sit in on and take notes on. The specific type of teaching can be listed alongside `Teaching`
			- `Lesson`
			- `Sermon`
			- `Lecture`
		- `MAP` 
			- This is for your Maps Of Content pages
		- `Note` 
			- The majority of your notes will have this tag. If it isn’t any of the other more specific types, it’s just `Note`.
		- `Source` 
			- This is for any external source that you plan to quote from.
		- `Book` 
			- Self explanatory. Use this if you have a single note for a book overall. 
			- Notes and reflections on individual chapters/sections should be typed as `Note` with tags handling the sorting.
		- `Person` 
			- This tag should be reserved for members. Biblical Characters, and  Pastors and Teachers all have their own type. 
		- `Teacher` 
			- This type is for keeping track of Pastors, Teachers, and Authors both living and past.

For a breakdown of Paraclete’s fixed `type`s, see [[Types|this page]].

### Person (member) specific front matter
This is possibly the page with the most fixed metadata. 
```yaml
---
type: Person
firstName:
middleName:
lastName:
nickname: 
birthday: 
locationMet: 
membership:
baptized:
volunteer:
vPosition:
sgMember: 
work:
email:
cell:
address:
city:
state:
country:
zipCode:
---
%%
spouse::
discipledBy::
discipling::
sgID::
smallGroupLeader::
smallGroupMembers::
%%
```
#### Definitions
- `firstName`: 
- `middleName`:
- `lastName`:
- `nickname`: 
- `birthday`: The birthday of the person. *Format:* `YYYY-MM-DD`
- `locationMet`: This is the place where the person was first met. Was it an event, Sunday morning in the lobby, or at a restaurant?
- `membership`: A simple yes/no as to whether or not the person qualifies as a Church member (if there are any qualifications for your setting).
- `baptized`: A simple yes/no as to whether or not the individual has been baptized in water. The specificty of whether or not they have been baptized in your own Church is dependant on your definitions and requirements.
- `voulteer`: A simple yes/no answer as to whether or not this person volunteers in any capacity.
- `vPosition`: This is the volunteer position held by the person.
- `sgMember`: A simple yes/no to indicate membership in an active Small Group.
- `sgGroupID`: The ID assigned to the person’s Small Group. More info [[Small Group Names|here]].
- `work`: The type of employment they have. For data retrieval purposes, single words work best. *ex:* Construction, Marketing, Mechanic, etc.
- `email`:
- `cell`:
- `address`: Street address.
- `city`: City of residence.
- `state`: 
- `country`:
- `zipCode`: 

There are also values defined using dataview’s inline declarations. These are variables whose defined value is a link to another note. 
By default these appear within a comment block, and are therefore invisible in Reading Mode. This can be changed by removing the `%%` at the beginning and end of the section.
- `spouse`:: A link to the page of the person’s spouse.
- `discipledBy`:: The person who is actively discipling this person.
- `discipling`:: The person/people this person is actively discipling.
- `sgID`:: A link to the page for their Small Group.
- `smallGroupLeader`:: 
- `smallGroupMembers`:: Only applicable of the person is a Small Group Leader. (I may remove this since it is redundant on the Small Group page)


### Lesson and Sermon specific front matter
```yaml
---
alias: 
origin: 
type: 
 - Teaching
 - 
title: 
date: 
location: 
teacher: 
topic: 
series: 
themes: 
passage: 
description: 
---
%%
teacher::
location::
%%
```
- `type`: Teaching
	- Lesson/Sermon/Lecture
- `title`:
- `date`: This is the date that the Teaching is scheduled to be taught. If the Teaching is given additional times, each additional date can be added as another value
- `location`: Where was this taught?
- `teacher`:  Who gave the Teaching?
- `topic`: What is the main topic of this Teaching?
- `series`: Which series (if any) was this Teaching a part of?
- `themes`: What themes where touched on in this Teaching?
- `passage`:  What was the main Passage used for this Teaching? Note that this is not a list of all passages referenced, the nested tags are used to track that.
- `description`: A brief description of the Teaching to show up in tables and previews.


## Inline Metadata

### How to Declare
Metadata can also be declared inline. This means that the values can be declared outside of the opening front matter section. This means that the declarations are visible in reading mode, and more importantly, links to other notes can be used and relationships preserved. 
An inline variable is declared with a double colon `::` rather than a single colon.
**example**:
```yaml
sgMembers:: [[Luke Skywalker]][[Han Solo]]
```

These can also be used in a way that is invisible, while still preserving the link and relationship. This is done by embedding the declarations in an Obsidian comment block.  In computer programming, a comment is simply a line of text that the computer ignores while executing the code. This is typically denoted with a symbol `//` `#` `/*` etc. followed by the text. These act as helpful reminders and descriptions for the programmer (or more often other programmers) to understand what the code does. In Obsidian this is done by using two prercent signs in a row `%%`.
**example**:
```yaml
%%
sgLeaders:: [[Ryan Green]] [[Stephanie Green]]
sgMembers:: [[Tom Bradford]] [[Sandra Olivers]] [[John Wick]]
formerMembers::
%%
```

If you would prefer to be able to see these values in Reading Mode, you can simply omit the `%%` before and after the variables.

Here are a couple examples of what this might look like in a note.
**Invisible:**
```yaml
---
alias: 
author: 
type: 
---
%%
invisibleInlineVariable:: [[Value that is another note]]
%%
```
**Visible:**
```yaml
---
alias: 
author: 
type: 
---
visibleInlineVariable:: [[Value that is another note]]
```

### What to declare
