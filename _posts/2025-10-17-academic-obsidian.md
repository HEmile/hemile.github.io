---
layout: post
title: How I use Obsidian for academic work
date: 2025-10-16 10:40:16
description: This post gives an overview of how I use Obsidian for academic research work. I use it to manage papers, talks, topics, concepts and projects in a Knowledge Graph-inspired setup. This setup is battle-tested in real-world academic use (5+ years of succesful use), so you might learn some useful tips and tricks.
tags: productivity
categories: productivity
---

I am a big of [Obsidian](https://obsidian.md/). 
This used to be some niche tool five years ago, but now it seems like every new PhD student comes in with Obsidian installed. 
And for good reason! It is an extremely powerful tool for managing your academic knowledge work. 
I've used Obsidian since 2020 (COVID...) and optimised my workflow to the point where I haven't had to make major changes in years. 
But while I was figuring out my setup, I developed and contributed to [several](https://github.com/HEmile/juggl) [popular](https://github.com/mdelobelle/obsidian_supercharged_links) [plugins](https://github.com/SkepticMystic/breadcrumbs)!
As many colleagues asked me about my Obsidian setup, I decided to finally get around to writing it down. 

A lot is written about how to best use Obsidian
However, those are rarely a great starting point for how I actually work in Obsidian, as I do not base my setup on a popular personal knowledge management methodology like Zettelkasten/linking your thinking/atomic/evergreen notes/etc. 
Each of these systems have great ideas but are too... bloated, rigid, or abstract for my taste. 
My setup is as simple as it could practically be while achieving a clear goal, namely to keep track of academic literature and ideas. 

I would say it is **battle-tested** in real-world academic use to such a degree (5+ years of succesful use) that I am happy to share it. 
I added **2100 papers** across **900 hierarchical topics** discussing **1600 concepts** to my vault, and collected 150 ideas for new projects. 
The vault is centered on making it easy to retrieve information, and every day I exploit my vault for finding relevant literature, new ideas, connections between concepts and people, and so much more. 
I still frequently use notes created many years ago. 
Furthermore, my setup is technically quite minimal, and instead centred around structuring connections between notes for effective academic work. 
In practice, only 3 community plugins are important!

<img src="/assets/img/obsidian-screenshot.png" alt="Obsidian screenshot" style="width:100%; height:auto;" />

In this blog post, I'll overview my workflow. 
This post is not an introduction to the basic note-taking features of Obsidian. 
For that, there are many good resources, in particular the [Obsidian Help vault](https://help.obsidian.md/install), but there is no need to become an expert in Obsidian before starting. 
Finally, this setup is what works for me. You can use it as a starting point, or integrate some ideas into your own vault. 
But play around, and see what sticks!

# The high-level overview
I prepared a [template on Github](https://github.com/HEmile/academic-obsidian) with everything below installed and configured, and with a few example notes (sneaking in some shameless self-promotion of my work ;)). 
If you want to see some examples, download it, and open it as a folder in Obsidian. Then browse around a bit, both in the file browser and using backlinks. 

The central idea behind my vault is to see it as a [knowledge graph](https://en.wikipedia.org/wiki/Knowledge_graph) built out of notes. 
Each note is a node in the graph with a particular type, and a few simple **typed links** between nodes semantically connect them. 
Let's start with the main types, which I indicate using tags. 
- `#source/paper` indicates notes about papers. Here, I will summarise and criticise the papers I'm reading _in my own words and understanding_. 
- `#source/talk` is similar, but for talks I attended. 
- `#topic` indicates the note is about a high-level topic. Papers and talks can be about that topic.
- `#concept` are notes about particular concepts relevant in your field. I use them to define concepts and define their relationship to other concepts.
- `#project` are notes about projects you are working on. I use them to keep track of the progress of my projects and ideas (these get the tag `#project/idea`).

I will introduce other types of notes as we go along. 

The central point of the vault is to **link maximally** between notes. This greatly increases the discoverability of your notes. 
So, seriously: For every paper you read and want to refer in your notes, create a note and link to it. 
For every concept you want to discuss, make sure to put it in brackets, even if you haven't created that note yet. 
Link everything! 

Linking greatly pays off because you can use [Backlinks](https://help.obsidian.md/plugins/backlinks) and [Notebook Navigator](https://github.com/HEmile/notebook-navigator) to (re)discover related notes and connections between your ideas and understanding. 

# Types of notes
Next, I'll go in more detail for each type of note and how I link them together. For each, I will provide an example from the [template on Github](https://github.com/HEmile/academic-obsidian). Creating each type of note is easy: Use `cmd + R` to open the [template modal](https://help.obsidian.md/plugins/templates), choose the note type, and hit enter.
You might notice each note type has a colour associated with it. I'll explain how this works in the Plugins section below. 

## Paper notes (blue)
<img src="/assets/img/paper-example.png" alt="Paper note" style="width:90%; height:auto;" />

Here is an example of a note about a paper of mine. 
The title of the note is always just the title of the paper (I do the same for talks). 
Then, you can see a whole bunch of metadata ([Properties](https://help.obsidian.md/properties)). 
- `aliases`: [Aliases](https://help.obsidian.md/aliases) is probably the **most underused but powerful feature** in core Obsidian. 
They allow you to create multiple names for a note. 
That is specifically very useful because when you are writing a note and want to link to some concept, you can open brackets with `[[`, and aliases will come up as suggestions in case you use a different spelling, a related term, or a synonym. 
Aliases also allow you to group together related concepts into a single note, such as when a paper introduces a new concept or method. 
Finally, Obsidian can show unlinked mentions of aliases among the backlinks to improve the linking between notes. 
- `hasTopic`: This is the first example of a **typed link** between notes, where the link type `hasTopic` provides additional semantic information about the link. It is the most important property for discoverability. I often have practically empty paper notes with just this field filled in so that it is indexed and easy to find and navigate to. Note that you can (and should) include multiple topics in this field! 
- `author`: A typed link to author notes, indicating they authored the paper. Author notes are just notes with the tag `#author` and where they work. This may seem like hassle at first, but having author notes is surprisingly useful for networking! Whenever I am (re)meeting someone, I check which of their papers I read and what I liked about them. 
This can also inspire useful new ideas for collaborations. 
I also use author notes to track where and when I met someone to reduce the amount of instances of "where did I know you from...". 
- `project`: This is a typed link to project notes for which the paper is relevant. 
- `publishedIn`: This is a typed link to a note for the journal or conference in which the paper was published. 

After that comes the main content of the note. In this example, I summarise the paper, linking to relevant concepts discussed in the meanwhile. I also often give my opinion of the paper for future reference. 

This might sound like a lot of work to manage for each paper, but plugins like [Templater](https://github.com/SilentVoid13/Templater) and, in particular, [the citations plugin](https://github.com/hans/obsidian-citation-plugin) make this seamless. I will explain in the Plugins section below how I set those up. 

## Topic notes (orange)
<img src="/assets/img/topic-example.png" alt="Topic note" style="width:89%; height:auto;" />

Most of my topic notes are very simple, containing at best a few sentences to describe and define the topic, preventing confusion with other topics. If you are familiar with 
hierarchical tags in Obsidian, a topic note is a note that sort of 'reperesents' a tag, except you can also add information about the topic.

The most important typed link for topic notes is `subset`, which creates a [hierarchy](https://en.wikipedia.org/wiki/Taxonomy) of topics (precisely, a [DAG](https://en.wikipedia.org/wiki/Directed_acyclic_graph)). Topic notes that are not subsets of other topic notes are the roots of the taxonomy and appear at the top level of the navigator.

For example, the topic of "reasoning shortcuts" studies a specific problem within neurosymbolic learning. And this problem relates to identifiability. And the topic of "artificial intelligence" is a root topic that contains many subtopics like "machine learning", "planning", "symbolic AI", etc. 
Note that such hierarchies are not possible with folders or hierarchical tags, as shown below. You can only put notes in a single folder. And hierarchical tags are only trees, meaning you cannot create topics like "neurosymbolic AI" as a subtopic of both "symbolic AI" and "machine learning":
<!-- Identifiability is actually a concept note, so I am not that strict about the function of each type of note and do whatever is fast and works best. -->

<img src="/assets/pdf/typed_links.pdf" alt="Typed links" style="width:100%; height:auto;" />





When you use `hasTopic` from papers and talks to link to topic notes, they automatically appear in the backlinks of the topic notes, and in the navigator on the left! Read below for other tips on how to use the notebook navigator to find notes related to a particular topic.

## Concept notes (green)
<img src="/assets/img/concept-example.png" alt="Concept note" style="width:70%; height:auto;" />


Concept notes describe and define concepts. 
A typical workflow is when I read a paper that discusses a new concept, I create a new note for that concept so I can refer to it in other notes. 
This also allows me to make connections between papers that discuss some concept from different perspectives. 

I use an exorbitant number of `aliases`, as you can see in this example: A monotone function, for example, can be monotone because it is increasing or decreasing. It is really not needed to make separate concepts for those, as these concepts are highly related and should be grouped together. 
I mainly use two types of typed links: `hasTopic` indicates the field of study that this concept is relevant for, and `isA` provides a hierarchy of concepts. In this example, monotonicity is studied within mathematics, and a monotone function is a particular type of function. 
Both `hasTopic` and `isA` will allow the note to appear in the navigator under the relevant topics. 



## Project notes (red)
<img src="/assets/img/project-example.png" alt="Project note" style="width:70%; height:auto;" />

Project notes will discuss the progress of an ongoing project, or describe an idea for a new project (in which case they get the tag `#project/idea`). 
I use the `with` typed link to refer to author notes of people involved in the project. 
I also use this to indicate who I had some idea with. This saves me from going behind someone's back on their own idea because I forgot where I got it from. Now I can ask for a collaboration, help or feedback! (This might sound like a niche thing, but as you progress your career, you will thank me for this tip.)
Project notes also have the `hasTopic` typed link as usual, and I use a lot of `aliases` for rediscoverability of ideas. 

For ideas, I also have a `score` property to rank them in 1-5 (I rerank them every year or so when I have to decide on master thesis topics). And another for the `size` of the idea. 

# Technicalities and tips
The rest of the post is going to be some random collection of plugins, hotkeys, tips, further minor explanations and answers to questions. 


## Plugins
I frequently see people online using dozens of plugins and chasing the latest cool features. 
However, at this point core Obsidian is progressed so far that I do not need many for the majority of common workflows. 
I would recommend only adding a new community plugin if you have a specific pain point that is not solved by core Obsidian. 

I will first discuss the plugins I use on a daily basis, and then a few optional ones that might suit your workflow. 

### [My fork of Notebook Navigator](https://github.com/HEmile/notebook-navigator)
[Notebook navigator](https://notebooknavigator.com/) is my most recent addition. 
It is an excellent and well-designed new plugin that replaces the file browser, search, bookmarks and tag panel for an Evernote-style layout. 
However, it is not compatible with the setup described above, as the navigator is based on folders or tags rather than typed links. 
Therefore, I [forked](https://github.com/HEmile/notebook-navigator) it and made it compatible with my typed-links centric structure. 
It comes preinstalled in the [template](https://github.com/HEmile/academic-obsidian), so I would suggest giving it a go there!

This fork instantiates the hierarchy of topics, and recursively adds notes with that topic (or that use `isA`) to the navigator. 
You can navigate it just like with tags, giving an immediate overview of the structure of your vault and the connections between your notes. 
When is this useful? 
Well, let's say you want to find all papers about the topic `Artificial Intelligence`. 
Without the navigator, you could navigate to the topic note `Artificial Intelligence`, and find its backlinks. 
But then you would be missing papers that link to the subtopic `Neurosymbolic Artificial Intelligence` but not to `Artificial Intelligence`. 
In the notebook navigator, you can hierarchically navigate through your vault, and find the papers about `Neurosymbolic Artificial Intelligence` together with other `Artificial Intelligence` papers within a single list!


### [Supercharged Links](https://github.com/mdelobelle/obsidian_supercharged_links)
This is my favourite plugin - but I also contributed heavily to it, so I might be a bit biased. 
You might have noticed from my examples that links have different colours depending on the type of note they are (practically: what tags they have). 
This is because of this plugin! 
It's honestly a huge life-saver: When I scroll through a search, or look at a note, I can immediately see if it is a paper, a concept, a project, etc. 
So when I search for something specific, I can open the quick switcher and visually filter by one of the colours without having to type an explicit filter. 

In addition, I programmed a few extras for my vault, such as paper links that indicate the year of publication and the venue they were published in, and ideas notes showing their score. 
Setting this up is not hard, but requires a bit of tweaking with CSS. 
I would suggest to start with the [template](https://github.com/HEmile/academic-obsidian) and work from there. 

### [Citations](https://github.com/hans/obsidian-citation-plugin)
The citations plugins are known for their integration with Zotero or bibtex files. 
That is what I also used... But honestly, it was too slow. Waiting for Zotero to import a file took too long, and so did syncing that with Obsidian. 

Instead, I use a custom-built version of this plugin available [here](https://github.com/HEmile/academic-obsidian/tree/main/.obsidian/plugins/obsidian-citation-plugin), which is preinstalled in the [template](https://github.com/HEmile/academic-obsidian). This adds a new command and hotkey to **directly create a paper note from a bibtex entry on your clipboard**. 
Then, I just find a bibtex entry online, copy it, hit the hotkey, and voila! 
This automatically adds the year, authors and citekey:

{% include video.liquid path="assets/video/citations-plugin.mp4" class="img-fluid rounded z-depth-1" controls=true width="80%" %}

### Other really useful plugins
These come pre-installed with the [template](https://github.com/HEmile/academic-obsidian). I use them every day, but are not necessary for the setup. 
- **Templater**: I use it more extensively for my personal vault, but it's always a very useful extension to [the templates feature in Obsidian](https://help.obsidian.md/plugins/templates) for automatically adding timestamps to my notes and getting cursors on the right place. 
- **Extended MathJax**: Add a preamble for your latex equations. I use this a lot for eg boldfaced math. Only important if you're in a math-heavy field. 
- **Omnisearch**: A replacement for the built-in search. It's blazing fast and clear, and works on PDFs. 
- **Pane relief**: This is such a staple for me that I always forget what it does unless I turn it off and get super frustrated. I hope that's enough of a recommendation.
- **Paste URL into selection**: Simple, select some text, insert a link to it by pasting.

### Optional plugins
Here are some other plugins I played with that are good, but are not core to the workflow.  
Please read on. 
- (Core) You'll need some way to sync and backup your vault. I just use **[Obsidian Sync](https://help.obsidian.md/sync)**. It has never failed me.
- (Core) **Bases**: This is a new feature to create database-like views from your notes. I haven't played around with it enough to see if it'll stick, but it sure is well-built! However, many people seem to rely on it. The setup I described above actually barely relies on it - The core navigation and search is really based on the graph structure (ie, navigating links in notes and navigating backlinks). Therefore, I only end up using database-like views for specific use cases like reranking ideas. 
- (Core) **Canvas, Graph view**: Honestly, these are fun to play with, but I never use them. GUI-based things are just too slow compared to plain text and keyboard shortcuts. 
- (Core) **VIM** support: I love VIM. If you like VIM as well, activate it. The VimRC plugin is a great complement. 
- **[Breadcrumbs](https://github.com/SkepticMystic/breadcrumbs)**: This plugin is the first major plugin for navigating your notes as a graph (more specifically, a DAG). This was pretty useful for my setup. However, the UI is nowhere near as user friendly and fast as Notebook Navigator, so I don't use it anymore.
- **[Juggl](https://github.com/HEmile/juggl)**: This is an advanced graph view plugin I developed. Therefore, you might expect me to use this. But honestly, it was just too slow and clunky for daily use. Fun to play around with, and it might work for you, but I wouldn't necessarily recommend it. 
- **[PDF++](https://github.com/RyotaUshio/obsidian-pdf-plus)**: Many people annotate their PDFs in Obsidian and try to link it together. I find it too cumbersome for the vast majority of papers, but this plugin really is excellent if you do prefer that workflow. 



## Hotkeys
Some important hotkeys that come pre-installed with the [template](https://github.com/HEmile/academic-obsidian) (for Mac):
- `cmd + O`: Open quick switcher
- `cmd + control + O`: Open omnisearch
- `cmd + Enter`: Open link under cursor in new tab (seriously great together with VIM)
- `cmd + P`: Open command palette
- `control + option + shift + I`: Create paper note from clipboard containing bibtex
- `cmd + R`: Insert template
- `control + O`: Navigate backward
- `control + I`: Navigate forward
- `cmd + J`: Hide/show left sidebar
- `cmd + K`: Hide/show right sidebar
- `cmd + shift + J`: Open and focus Notebook Navigator
- `cmd + D`: Reveal current note in Notebook Navigator's topic graph
- `cmd + T`: Open new tab
- `cmd + W`: Close current tab

## Other types of notes
Some other types of notes I use that are mostly quite similar to the four ones described above. 
Maybe for your workflow, these could inspire which ones to add. 
In general, I would suggest a note type (ie, tags) to be for categories (e.g. a human, a paper, a talk, a concept, a tool), but not about something specific like a field of study (about biology, about mathematics, about life, etc). 
If you're a botanist, a `#plant` tag is probably a good idea. 
- `#source/dataset`: Notes about datasets and benchmarks. 
- `#method`: Within AI, we often compare specific methods at their performance. Many papers introduce a method. I find it is unnecessary to have separate notes for the paper and the method it introduces. So this is a type I actually rarely use, and only for very established methods. Instead, I usually add the method name as an alias. 
- `#method/tool` and `#method/library`: Notes about tools and libraries that can be used in academic research.
- `#concept/problem`: Notes about open problems that are studied in the field.
- `#venue/conference`: Notes about conferences and journals (`#venue/journal`).
- `#institution`: Notes about institutions like universities or companies.

## Question - Answers
Anything else? You know where to find me. I hope. 
- **Do you recommend I just use this template as is?** 
My recommendation is that you start off with some structure in your notes, even if it's different from that described here. 
A common refrain in the Obsidian community is to 'just write notes' and add extras later. 
I agree with that comment if it's about adding unnecessary plugins and features, but thinking up-front about the structure of your vault will pay off. 
It is significantly easier to restructure an already structured vault, than to introduce structure to a bunch of notes without structure. 
- **How about todo management?** I tried it, way too cumbersome. I just use something stupid like Microsoft To-Do now. Keeping todos within project notes for specific detail tasks or reading lists can be useful though. 
- **How about meeting notes?** I find doing this in Obsidian is actually often not that useful. Meeting notes are very temporary, and can 'dilute' your vault as they only stay relevant for a few weeks. And they're most useful when shared with others. Obsidian is single-user and sharing markdown files around is just... Annoying? If anything, I sometimes put some action items in my project notes, depending to the degree of communication and infrastructure of the project. 
- **What do you think about \<latest plugin X\>?** I do not closely follow all the latest plugins as I do not currently have any real pain points in my Obsidian setup. Well, there is one: I don't have enough time to build and maintain my notes because academic life is so hectic. But I'm afraid no plugin is going to fix that.
- **How about things that are not academic work?** I could write a whole another blog post about this. I also have a very nice setup, quite similar in spirit to this one. But its main issue is in the previous answer. 
- **Not even LLM plugins??? I thought you worked on AI?** Look, I don't use them. I might integrate one when it can understand the hierarchical structure of my notes via some RAG system, but right now it's just not good enough. And seriously, **do not use LLMs to write your notes**. The whole point of taking notes (and learning!) is to write them in your own words, and to go back and view [what **you** understood about it](https://stephango.com/understand). (I am not an LLM hater, I use them all the time for QA, coding and assisted writing, just never in Obsidian.) 
- **What is your folder structure?** I only use tags to indicate note types. I do not use any folder structure, all notes are in the top-level directory. Folders are strictly hierarchical, and create walls between ideas. Furthermore, it is not worth the effort when you are already using links to structure your vault. 
- **Do you have index notes / maps of content?** Nope, not worth the maintenance time imo. Going through backlinks and simple search is sufficient for retrieval. 
- **Should I create a separate note for concept or topic X? Or put it as part of note Y?** 
I don't have any real guidelines here; it's just gut instinct at this point. If I think a note gets too bloated, I sometimes split it up. But I also don't want all kinds of mini notes about the most niche concepts. 
Most importantly, **don't overthink this**: 
Merging and splitting notes when you already have a structured vault is pretty fast, you just go through the backlinks and update some links. 
- **How long should my notes be?** 
This is definitely something you'll develop over time. 
In practice, the majority of my notes are very short, maybe containing a few sentences and a nice figure from a paper. The main goal is to index it in the vault via typed links. 
But I describe other papers and concepts with a lot of detail and can be many pages long. Usually it just depends on how relevant it is to my current work. 
- **Do you have a 'note maintenance' / evergreen note strategy?**
Yes, but it's simple: If I am writing new notes and linking, and then finding a mistake or outdated views in a related note, I update it. But I don't go out of my way to do this. 
- **How do you manage your attachments?** I don't, I just put them all in the `files` folder. All my attachments are images I paste into notes. I'm too scared to look into the `files` folder, truth be told.  
- **Do you clip sources or save pdfs?** Nope, too much overhead. 
- **Oh not another AI dude giving advice about _all of science_.** 
Obviously, I have no idea if these ideas transfer to other fields. 
But I would guess so! 
You might need to add a few more note types that are relevant to your research (e.g., particular types of proteins or plants, or years, or historical periods, etc etc.). 
In my personal vault, I actually have _way_ more note types and it works just fine. But the idea of structured typed links just comes from knowledge graphs, and those are also applied in biomedical sciences, digital humanities, social sciences, etc. 
- **That [example vault](https://github.com/HEmile/academic-obsidian) is cool and all but very empty. Can you share your actual vault instead?** No, sorry. Those notes are... A bit unfiltered, if you know what I mean :). I don't have time to make it presentable. And honestly, my vault is part of my academic human capital! But here is a screenshot:
<img src="/assets/img/own-vault-example.png" alt="Vault screenshot" style="width:100%; height:auto;" />