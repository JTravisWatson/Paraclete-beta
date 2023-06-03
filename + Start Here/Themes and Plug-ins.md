# Themes and Plug-ins
This vault has been purposefully left with only it’s default theme, and the `dataview`, `templater`, and `tag wrangler` plug-ins installed. Nothing further is really needed to use the Paraclete System, but that doesn’t mean it is forbidden or even discouraged.

## Themes
Themes change the appearance of Obsidian. That sounds simple, but they can also do so much more. And why would you change the theme? Why not? If having a certain color scheme, or layout helps you focus and get work done, or even just makes it more fun to work, than go for it. 

I’ve broken this down into two categories, Destructive, and Non-Destructive.

>[!tip]
> Before you install any theme, it is recommended that you first install the `Style Settings` plug-in. This allows a lot of themes to be customized, and unlocks their real potential.



### Destructive
Destructive Themes are any theme that go beyond a simple re-skin of the application. Some themes change the workflow, add their own CSS Classes, and even their own unique functionality. These kinds of themes are great for making Obsidian feel like other programs, which can be helpful if you are coming from another platform like Notion, iA Writer, or if you are just looking for a different experience.
**Examples:**
- 

### Non-Destuctive
Non-Destructive themes are the simple recolors of Obsidian. While these themes can sound less exciting, they are safer and more future proof. Chances are your tastes and workflows will change over time, and these themes account for that. 

Let’s say you have a Destructive Theme, and you get used to using its unique callout, or Dashboard style CSS Class, but in the future you change themes and workflows. Now, all of your notes written with that previous workflow don’t function like they did before. In a sense, you can get “locked-in” to a Destructive theme.
**Examples:**
- 

### Minimal Theme
I’m putting this theme as its own subheading. The reason is that this theme is the most popular community theme, has its own `Minimal Theme Settings` plug-in, and is only as destructive as you want it to be.

## Plug-ins
Plug-ins are the **real power** of Obsidian. You can extend its functionality to be as specialized (or as broad) as you want it to. While it is tempting to start adding every cool looking plug-in, it is advised that you refrain from adding them wherever possible. Initially, use this Vault as-is for a couple weeks and identify any friction points that might be alleviated by a plug-in, and then add just that one plug-in. 

Each plug-in you install adds a certain layer of complexity and potential instability to your setup. Since the plug-ins are community built and maintained, they are not updated along with the core program. Sometimes an update on one plug-in can break the functionality of another. The community developers of Obsidian are a very active and open community, so these issues are typically resolved quickly, but this is still something that you should be aware of.

### Required Plug-ins
- [`Dataview`](obsidian://show-plugin?id=dataview)
	- Duh
- [`Templater`](obsidian://show-plugin?id=templater-obsidian)
	- Also Duh

### “Must have” (but not required) Plug-ins
These are plug-ins that will almost certainly enhance your workflow. While they aren’t needed for Paraclete, they add some tangible value.

- [`Tag Wrangler`](obsidian://show-plugin?id=tag-wrangler)
	- This plug-in almost made the required list. It helps to manage tags, and makes working with nested tags a breeze.
- [`Bible Refernce`](obsidian://show-plugin?id=obsidian-bible-reference)
	- This plug-in could easily be used in place of the [[Expansions#The Bible in Markdown| The Bible in Markdown]] Expansion. It uses a public API to fetch the text of whatever verse, verses, or chapter you search for, and produces a callout stylized to how you configure it in the preferences.
- [`Periodic Notes`](obsidian://show-plugin?id=periodic-notes)
	- Great for creating Daily, Weekly, or Monthly notes from a template. If you are big into journaling your devotions, this is the plug-in for you. It can also be used as another type of hub note, or catch-all. Make a new note every day, dump your ideas, meeting notes, and reflections into it as you go (possibly on mobile), and than refactor everything to where it will live permanently at the end of the day.
- [`Calendar`](obsidian://show-plugin?id=calendar)
	- Adds simple Calendar functionality. There are several of them, so check them out to see how they might integrate into your workflow, especially if you use Daily Notes.
- [`Quick-Add`](obsidian://show-plugin?id=quickadd)
	- Allows more advanced users to create macros to quickly add new notes and execute commands.
- [`Buttons`](obsidian://show-plugin?id=buttons)
	- This in combination with `Quick-Add` and `Templater` just makes sense. Add buttons to execute Macros, such as “Create New Person”, “Create New Lesson”, or anything else you can think of.


### Helpful Plug-ins
- [`List Callouts`](obsidian://show-plugin?id=obsidian-list-callouts)
	- Turn bullet points into highlighted callouts with icons. Don’t underestimate what this plug-in can do, especially if you are a bullet point junkie.
- [`Text-Generator`](obsidian://show-plugin?id=obsidian-textgenerator-plugin)
	- This one is pretty neat. It uses the GPT AI to generate text in your notes. It requires an OpenAI account, and uses money (starts with some credit), but the results are pretty great. Definitely not to be relied on for theological conclusions, but for outlines, summaries, and comparisons, this plug-in is pretty awesome. For personal and occasional use, it will cost mere cents to integrate. For example, I found that after 3 months of pretty heavy use, I had only used $0.70 of compute time.
- [`Advanced Tables`](obsidian://show-plugin?id=table-editor-obsidian) 
	- Easily the biggest weakness of Markdown, and therefore Obsidian, is working with tables, at least those *not* generated by `dataview`.  Advanced tables helps you more easily create, edit, and navigate pure markdown rables.
- [`Sortable`](obsidian://show-plugin?id=obsidian-sortable)
	- This adds the ability to toggle which column of a table is sorted, and how (ascending, descending, default). This also applies to `dataview` tables. Sometimes it’s the little things that make a difference. 

### Just Plain Cool
- [`Banners`](obsidian://show-plugin?id=obsidian-banners)
	- Add a photo banner to the top of a note. This gives a look similar to Notion. I like to use this to make my Dashboards and MAPs visually stand out from the standard note. 
- [`Highlightr`](obsidian://show-plugin?id=highlightr-plugin)
	- Creates multiple highlighter colors. This is a great way to transfer physical notes if you also use multiple highlighters to emphasize things differently.
- [`Tasks`](obsidian://show-plugin?id=obsidian-tasks-plugin)
	- An incredibly powerful way to make, track, and complete tasks in Obsidian. If you are looking to make Obsidian your main tool, than this is an easy choice.
- [`Obsidian Icon Fodler`](obsidian://show-plugin?id=obsidian-icon-folder)
	- Add icons for each folder. Simple but fun. This is helpful for the more visually minded people out there.

## CSS Snippets
Obsidian is written using Electron, meaning its built on web technology. This means that both HTML as CSS can be used to enhance Obsidian. HTML will even render natively in the editor.

CSS Snippets fall somewhere between a Theme and a Plug-in. And in fact, both are written using plenty of CSS and CSS Snippets.

Think of CSS Snippets as just little Lego bricks of functionality that we can add to our vaults to change a single feature. CSS Snippets can be activated from `Settings -> Appearance -> CSS Snippets` in the main Settings menu. 

> Dealing with CSS Snippets is definitely for more advanced users, but don’t be intimidated.

## Expansions
More dramatic expansions are explained [[Expansions|here]].