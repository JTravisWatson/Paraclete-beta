
# The Paraclete System

> [!note] Paraclete
> An advocate
> A helper

## What is the Paraclete system?
The Paraclete System is a framework of naming standards and workflow within Obsidian, and is meant to be a tool to help Bible teachers, Pastors, and Small Group teachers to enable them produce more focused, enriched, and consistent lessons. The system leverages the program [Obsidian](https://www.obsidian.md), along with a couple of its plug-ins in order to make this tool as powerful as possible.

>[!tip|]- My Heart
>Personally, my passion is for the Word of God and seeing it taught well. 
> 
> I hope this tool is as useful to the Presbyterian as it is to the Pentecostal. 
>  
>  To that end, my aim is to create a system that can be tailored to individual teaching styles, service structures, and contexts without “drawing any lines in the sand” theologically speaking. That doesn’t mean I don’t have my own, of course, just that I hope to keep them out of this tool so that it might be used by God in as many places as He sees fit.

**The Paraclete System has multiple parts.**
1. The set of naming standards
2. The overarching workflow

Paraclete can be used as either just `1`, or as `1 & 2`. 

We’ll take a look at the two major components, though we will look at them in the reverse order of how we presented and numbered them above. I hope the reason for this becomes apparent as you read.

## The Overarching Workflow

Your Obsidian Vault/PKMS should have a point, a reason to exist. As believers, we have the strongest reason to connect our thoughts, notes, and outputs (lessons). Ultimately the goal of the Paraclete system is to create a workflow for the Pastor, Teacher, or study group leader where time spent studying is maximized, previous efforts aren’t wasted, and personal engagement can be increased.

For a more detailed breakdown of the workflow, see [[Workflow|this page]].

### Folders
The naming convention for Folders is fairly loose in Paraclete. That will be made more clear below.

#### Folders on the Root
As far as Paraclete is concerned, there should only be 4 folders on your root `/`. 

`1 Lessons` - Where the Teachings being prepared are stored
`2 Maps` - A folder to contain your `Maps Of Content`, or Index pages
`3 Archives` - Your personal Jedi Archives where all your non-lesson and non-MAP notes live
`4 System` - This contains folders necessary for Obsidian. Namely `Attachments`, `Templates`, and your `Bible in Markdown` Folders

>[!tldr]- Alternative structure
>If you are using this system contained within another Vault, say in a subfolder like `Paraclete` or `Lesson Prep`, etc. than you can treat that subfolder as the root for these names.

Th reason these folder names are important is because of the `dataview queries` present in other notes. We can make calls like `FROM "1 Lessons"` because we know that the name of the lesson folder is `1 Lessons` regardless of the user. 

For example, a query that displays all of your upcoming teachings would look like this:
```sql
TABLE without ID
	file.link AS "Teaching",
	type AS "Type",
	date AS "Date",
	description AS "Description",
	topic AS "Topic",
	series AS "Series",
	teacher AS "Teacher",
	themes AS "Themes",
	file.etags AS "Tags"
FROM "1 Lessons"
WHERE
	contains(type,"Teaching")
SORT
	date
```

Without a naming standard, this would not produce a meaningful output when placed in another vault.

We will take a look at the purpose and structure of each of these folders below.

##### 1 Lessons
This is the main reason the Paraclete System exists: to *help* you prepare your lessons with greater speed, richness, and with reduced stress. This is where your *FUTURE* lessons will live. 

There are two ways you could populate this folder:
1. Individual Lesson notes
2. Subfolders for each upcoming lesson

Again, we will look at these in reverse order.

###### Subfolders
Subfolders for each lesson can be used, and are helpful if the lesson needs accompanying files. For instance a slideshow, worship lyrics and chord charts, pictures, etc.. Remember, Obsidian is a Markdown editor working *on top of* files and folders on your hard drive. This means that the entire lesson subfolder can be shared with whoever needs the associated resources, even if they don’t have or use Obsidian. As always, adapt this to your personal needs.

>[!tldr]- More than just Lessons
> If, like many of us, you serve in multiple roles and are required to plan or schedule more than just Teachings, than this system can be easily adapted. Simply add `Event` as a “teaching type” in the naming convention. For example `2023-06-10-EVENT-Fish Fry` could be used alongside the upcoming Sermons and Lessons. I would advise caution here as to how many “types” you add. For instance, meetings and 1-on-1’s don’t need to crowd this folder.

If using subfolders, the subfolder name should follow the pattern `date of lesson/sermon(yyyy-mm-dd)-TYPE-Series-Title`. Not all components (such as Series Name) may apply to all subfolders. Skip if not needed.
**Some examples:**
- 2023-05-14-SERMON-The questions of Jesus
- 2023-08-16-LESSON-Foundations-The Holy Spirit in the Believer
- 2023-06-14-LESSON-Ephesians Chapter 2 week 1

The associated Teaching note within should follow the same naming convention as the subfolder.


###### Individual Files
Alternatively, you can simply populate the `1 Lessons` folder with an individual note for each upcoming Teaching. As with the subfolder setup, each lesson follows the same `date of lesson/sermon(yyyy-mm-dd)-TYPE-Series-Title` structure.

##### 2 Maps
As stated earlier, this folder contains the `Maps of Content` and indexes for the Paraclete System. Some examples of MAPs might be `Biblical Themes MAP`, `Apologetics MAP`, `Heresies MAP`, or even a `Lessons and Sermons MAP`. Repeatedly navigating in a top down matter from `Broad MAP` -> `Focused Area` -> `Specific Content` helps to reinforce the subject’s location both physically in your vault, as well as where it fits in the subject matter.

Because of the consistent naming and metadata in all of our notes, these MAPs can be generated dynamically using `dataview` queries. Simply create a `type:` or `tag` with your desired category, and create a map that calls up those pages. With the ability to add multiple types and tags to each note, a single note can be navigated to via multiple MAPs. For example, you may end up at a page about `Isaiah` via the `Prophets MAP`, `Bible Books MAP`, or even . Feel free to add multiple `types` and `tags` to a single note. this costs nothing, burns no additional resources, and worst case you have some note descriptions that aren’t queried (yet).

This folder can easily be the most neglected, but after you learn this method of navigation, you’ll quickly be tempted to overpoulate it with some hyper specific MAPs, leading to the opposite problem.

##### 3 Archives
If you’ve been reading all of this thinking “This is way too much structure! My brain isn’t organized into neat boxes like this”, then you’ll be glad to hear that `3 Archives` is basically your playground. As far as Paraclete is concerned the internal structure of `3 Archives` could be literally anything. According to Paraclete’s Standards, all dataview queries and links will rely on metadata and tags rather than file paths (at least never deeper than the root folders like `3 Archives`).

Because Paraclete uses fixed naming conventions and set metadata variables you *could* simply dump all of your notes (daily notes, topics, meeting notes, book studies, people profiles, ideas, etc.) into this folder with no subfolders. I would strongly suggest you don’t. I would suggest using a system to organize your `3 Archives` folder. You could use [Johnny.Decimal](https://johnnydecimal.com/), [PARA](https://fortelabs.com/blog/para/), the general [LYT setup](https://www.linkingyourthinking.com/download-lyt-kit), or even a variation of the Dewey Decimal System that Libraries use.

##### 4 System
The system folder is there to hold folders and files necessary for the Paraclete system to operate, but don’t really need to be visible in searches and the graph view.

###### Attachments
From the main settings panel in Obsidian, point it to this folder as the system’s attachment folder. This way the system will automatically move any pictures, audio files, or other attachments here instead of spread all across your vault. This makes maintenance easier in the case that you move a note with attached images, but forget to move the images. 

###### Templates
Just like the `Attachments` folder, you can tell Obsidian that all of your templates live here. That way when you want to open a new note from a template, you only see the options from this folder, not your whole vault.

###### Scripture (Bible in Markdown)
Putting your entire copy of the Scriptures here makes things easier in a couple ways.

First, if you don’t want this this to show up in every search result, or graph view, you can simply exclude the entire `4 System`  folder.

Second, This produces 66 subfolder each with their own number of subfolders to crowd your vault. If you want your `3 Archives` to stay clean and organized, this is the place to keep your scripture files.


### Notes (*Not Teachings*)
Wherever possible, strive to have single word names for notes on “common” or “foundational” topics. Examples would be:
- `Jesus`
- `Grace`
- `Sin`
- `Divinity`
- `Prophet`
- etc.

Each Paraclete Vault should only have 1 note on these [[Core Concepts]]. This is to allow more consistent linking when sharing notes. For example, if you want to share a note you took on `Thematic Parallels between the Books of Joshua and Revelation` with another Paraclete user, your references to `Grace` and `Judgement` would link to their notes on the topic, rather than yours. If you wanted to link to your notes, you would simply use a more unique note name, reference those withing the note, and, obviously, share them as well.

For example If you are prepping a lesson on Grace, don’t name that lesson note `Grace`, but instead name it something more unique, descriptive, and memorable like `Grace, but at what cost?`

For notes more about how topics interplay, or their implications in our lives, feel free to use more unique and descriptive note names. The metadata and tag standards will help sort everything out. A great whay to do this is to name a note for the question you are attempting to research or answer within. for example, instead of a note named `Jacob Wrestled` call it `When wrestling with the angel, why did Jacob ask for a blessing when he had already been blessed?`

### Variables and Values
Variables are the *names* of the values being assigned, while the Value is the *data* within it. Think of it as the variable is the question, while the value is the answer. What `type:` of note is this? a `Sermon`. Written as `type: Sermon`.

#### Variables
Variables can appear in two places: front matter or inline. In either case, we will use the same naming conventions for each. All variable names will aim to be as concise and descriptive as possible. They favor single words, or two words written in “Camel Case”. Camel Case simply means capitalizing the first letter of the following words instead of using spaces. An example is `bibleBook`. *note:* `variables` cannot contain spaces, but `values` can. 

> [!tip|right-small]- Inline Variables
> As a rule of thumb, I reserve the use of inline variables for variables whose value is another note. 
> This preserves the relationship for backlinks, and the graph view.
> For example, if the variable is `spouse` the value is the page for that spouse. 
> This would be written as:
> `spouse:: [[Stephanie Green]]`

The predefined set of Variables can be found [[Data Model|here]].

#### Values
Values, in contrast to Variables, do not aim to be concise or without spaces. Wherever possible, Values can be capitalized, include spaces, and even be as specific as needed. Keep in mind that while the `variable` is what the program is looking for, the `value` is what is output and read by the user.

Some examples of `variable`:`value` pairs:
- `topic: Lifelong Learning`
- `date: 2020-04-15`
- `passage: Luke 4`
- `vPosition: Small Group Leader`
- `postal-zip: 78063`
- `baptized: Yes`
- `description: A page to describe the naming standards and conventions for files folders and subfolders.`

**Note:**
When defining values, a comma `,` will act as a separator between values. This will give you multiple separate values.

### Tags
Tags can be a powerful tool when used purposefully and consistently, or a jumbled mess when used haphazardly. Just like other `variables`, `tags` can be defined either in the metadata, or in the body of the note itself. When defined on the metadata, tags are written as `tags: Easter`, and when defined in the note itself the are simply written as #Easter . Like Values, tags should be capitalized and descriptive, though as Variables, they *cannot* contain spaces.

Tags are used in the Paraclete System for sorting, linking, and retrieving. While all of the core tags are listed and defined on the [[Tags]] page, we’ll take a brief look at their uses here.

#### Single Tags
Single tags are your common simple tag, they’re written as a `#` symbol followed by a single word. We’ve all seen it, and it’s use is fairly obvious. These single tags are great for noting which themes are in a lesson, or what holiday they’re about, or series.

#### Nested Tags
Nested tags are where the real power of tags can be leveraged in the Paraclete System.
Nested tags function like an invisible folder structure. That is, they can be nested like folders, without the tagged notes needing to be in those folders. This also means that one note can be in multiple places at once.

For example, when we tag a sermon, lesson, or reflection with the scripture reference it follows this structure: `Book/Chapter/Verse` -> `#Romans/12/2`. That means that that note appears in the “folder” for `#Romans`, `#Romans/12`, *and* `#Romans/12/2` as well as any other tags included in the note.

Other nested tag structures can be used. For example, let’s say that you regularly teach at a school and have various classes. We could use tags to sort and organize these lessons without the need for additional folders. Some examples:
- `#LibertyChristian/WorldReligions/Islam`
- `#LibertyChristian/EarlyChurchHistory/Unit1`
- `#LibertyChristian/WorldReligions/Wicca`
- `#LibertyChristian/EarlyChurchHistory/EssayPrompts`

All of the above examples would appear in the “folder” `#LibertyChristian` with each additional nested tag being more specific.

## Naming Standards and Conventions

By using an agreed upon set of standards, Paraclete becomes both internally consistent and interoperable with other users. **This is the real strength (and goal) of the system.** If we all agree to use the same variable names and conventions, then notes can be shared freely without “breaking” the system it is put into. Let’s say, as a teacher, you want to share all of your notes on the practices of the cultures that surrounded ancient Israel with all of it’s cross linking and dataview tables (where it makes sense). You could simply share your `John Draper’s Ancient Israel notes` folder, and other Paraclete users could paste the files into their vault knowing there would be minimal to no conflicts with their existing notes.


## Plug-ins and Expansions
The core Paraclete System aims to require as few plug-ins as possible. In fact, the only two plug-ins truly needed are `Dataview` and `Templater`, but to be honest, every instance of Obsidian should have these Installed.

### Plug-ins
There are literally hundreds (~900) of Obsidian Plug-ins, but only `Dataview` and `Templater` are really needed for Paraclete. Dataview generates the dynamic lists that make navigation through the MAPs possible. Otherwise, you would need to go in and add a new link on every page each time you made a note. That sounds like a gross waste of time. Templater saves time creating new notes by allowing more complicated (or specific) templates.

There are lots of plugins that enhance the experience and can be added later on to help your workflow. If you are new to Obsidian, take it slow and only add plug-ins when you encounter friction points in your workflow. Also, try to avoid adding any additional plug-ins for the first week or two.

#### “Must have” (but not required) Plug-ins
- `Periodic Notes`
	- Great for creating Daily, Weekly, or Monthly notes from a template. If you are big into journaling your devotions, this is the plug-in for you.
- `Calendar`
	- Adds simple Calendar functionality. There are several of them, so check them out to see how they might integrate into your workflow, especially if you use Daily Notes.
- `Tag Wrangler`
	- This plug-in almost made the required list. It helps to manage tags, and makes working with nested tags a breeze. In fact, if you are going to immediately install one plug-in, it should be this one.
- `Quick-Add`
	- Allows more advanced users to create macros to quickly add new notes and execute commands.


#### Helpful Plug-ins
- `Text-Gen`
	- This one is pretty neat. It uses GPT-3 to generate text in your notes. It requires an OpenAI account, and uses money (starts with some credit), but the results are pretty great. Definitely not to be relied on for theological conclusions, but for outlines, summaries, and comparisons, this plug-in is pretty awesome.
- `Banners`
- `Advanced Tables`
- `Sortable`
- 

### Expansions
These are just a few modules that greatly increase what’s available to you in the Paraclete System.

#### The Bible in Markdown
Not really a plug-in, and not really required, but the [Bible in Markdown](https://github.com/selfire1/BibleGateway-to-Obsidian) is incredibly useful. This is a bit more advanced, and requires some time in the command line, but the pay-off is huge. This script turns the entire Bible into a folder that can live in your vault. This allows links, and quotes all within your vault. Again, not required, but a real game changer.

#### Database Folder
This is a plug-in that makes Obsidian feel like a whole new program. This essentially allows you to turn a folder into a Notion-like database. You can create new entries, modify metadata, search, and sort all from the database view. This is the basis for the Member Database on my personal iteration of this system. What this can do is far beyond the scope of this write up.

### Themes
>What theme should be used? Whatever theme will help you get work done.

There are so many beautiful themes for Obsidian. Seriously, try some out, and settle on what works.

The [[Themes and Plug-ins]] note has more information on this topic.

## Resources and Inspiration

Of course, this idea didn’t come out of the blue. I took a lot of inspiration from other Christians maximizing their eficiency and talking about it. 

### Chris Wilson
[CJWilson](https://www.cjwilson.co.uk/set-up-obsidian-digital-bible-notes/)
Chris got me turned on to *why* I would use Obsidian as a Believer. His videos on connecting thoughts and notes combining Bible study and Obsidian are a great starting point.

### Joschua
[Joschua’s Bible Study Kit](https://forum.obsidian.md/t/bible-study-in-obsidian-kit-including-the-bible-in-markdown/12503)
My initial efforts began as retooling of Joschua’s Bible Study Kit. I had mangled his initial version to fit my workflow so much, the only thing left over was the Vault name, the Bible in Markdown, and the concept behind it. If the Paraclete System seems like a bit too much for you, than Joschua’s Bible Study Kit might be exactly what you’re looking for.

### Reagan Rose AKA RedeemingProductivity
[Redeeming Productivity]([https://www.redeemingproductivity.com](https://www.redeemingproductivity.com/))
While I don’t think Reagan is an Obsidian user himself, his Biblical insight on productivity, priorities, and work ethic definitely fit into the over all thrust of this project. His articles are great quick reads that always seem to find a friction point in my life that nobody else is challenging.

