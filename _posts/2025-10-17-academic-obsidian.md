---
layout: post
title: How I use Obsidian for academic work
date: 2025-10-16 10:40:16
description: Some description
tags: productivity
categories: productivity
---

I am a big of [Obsidian](https://obsidian.md/). 
This used to be some niche tool five years ago, but now it seems like every new PhD student comes in with Obsidian installed. 
And for good reason! It is an extremely powerful tool for managing your academic knowledge work. 
I've been using Obsidian since 2020 (COVID...) and have optimised my workflow over many years. I also developed and contributed to [several](https://github.com/HEmile/juggl) [popular](https://github.com/mdelobelle/obsidian_supercharged_links) [plugins](https://github.com/SkepticMystic/breadcrumbs) in the meantime!
Many colleagues asked me about my Obsidian vault, so finally got around to writing about it. 

First, I realise there are many blogs and posts about how to use Obsidian. 
Many of them are good, but honestly, my setup is not based on any popular system like Zettlekasten-based note-taking or some template from a popular Youtuber. 
I have no financial interest in promoting my way of using Obsidian, I am just happy to share it! 
Furthermore, my setup is battle-tested. 
My vault has **2000+ papers** across **1000+ topics**. 
My vault is centered on optimising for retrieval, and every day I exploit the database I built over my career. 
Furthermore, my setup is technically quite minimal, and instead is centred around structuring your notes for effective academic work. 
In practice, only 3 community plugins are central!

<img src="/assets/img/obsidian-screenshot.png" alt="Obsidian screenshot" style="width:100%; height:auto;" />

In this blog post, I'll overview my Obsidian vault. 
This post is not an introduction to Obsidian. For the basics, there are many good resources, in particular the [Obsidian Help vault](https://help.obsidian.md/install).
Finally, this setup is what works for me. You can read this blog post as a starting point, or just integrate some of its ideas into your own vault. But play around with it, and see what sticks!

# The high-level overview
I prepared a [template on Github](https://github.com/HEmile/academic-obsidian) with everything installed and configured, and with a few example notes (sneaking in some shameless self-promotion of my work ;)). 
If you want to see some examples, download it, and open it as a folder in Obsidian. Then browse around a bit, both in the file browser and using backlinks. 

The central idea behind my vault is to build a [knowledge graph](https://en.wikipedia.org/wiki/Knowledge_graph) out of your notes. 
Each note is a node in the graph with a particular type, and links between nodes are typed to have a particular meaning. 
Let's start with the main types, which I indicate using tags. 
- `#source/paper` indicates notes about papers. Here, I will summarise and criticise the papers I'm reading _in my own words and understanding_. 
- `#source/talk` is similar, but for talks I attended. 
- `#topic` indicates the note is about a high-level topic. Papers and talks can be about that topic.
- `#concept` are notes about particular concepts relevant in your field. I use them to define concepts and define their relationship to other concepts.
- `#project` are notes about projects you are working on. I use them to keep track of the progress of my projects and ideas (these get the tag `#project/idea`).

I will introduce other types of notes as we go along. 

The central point of the vault is to **link maximally** between notes. This greatly increases the discoverability of your notes. 
So, seriously: For every paper you read and want to refer in your notes, create a note, link to it. For every concept you want to discuss, link to it with `[[convex set]]`, even if you never create that note yet. Link everything! 
Linking greatly pays off because you can use [Backlinks](https://help.obsidian.md/plugins/backlinks) to discover related notes and find (or more likely, rediscover) connections between your ideas and understanding. 

I only use tags to indicate note types, but never for anything semantic. I do not use any folder structure. Folders are strictly hierarchical, and creates walls between ideas. Furthermore, it is not worth the effort when you are already using links to structure your vault. 

# Types of notes
Next, I'll go in more detail for each type of note and how I link them together. For each, I will provide an example from the [template on Github](https://github.com/HEmile/academic-obsidian). 
## Paper notes (blue)
<img src="/assets/img/paper-example.png" alt="Paper note" style="width:60%; height:auto;" />

Here is an example of a note about a paper (of mine). 
The title of the note is always just the title of the paper (I do the same for talks). 
Then, you can see a whole bunch of metadata ([Properties](https://help.obsidian.md/properties)). 
- `aliases`: [Aliases](https://help.obsidian.md/aliases) is probably the **most underused but powerful feature** in core Obsidian. They allow you to create multiple names for a note. That is specifically very useful because when you are writing a note and want to link to some concept, you can open brackets with `[[`, and aliases will come up as suggestions in case you use a different spelling, a related term, or a synonym. Aliases also allow you to group together related concepts into a single note, such as when a paper introduces a new concept. Finally, Obsidian can show unlinked mentions of aliases among the backlinks to improve the linking between notes. 
- `hasTopic`: This is the first example of a **typed link** between notes, where the link type `hasTopic` provides additional semantic information about the link. It is the most important property for discoverability. I often have practically empty paper notes with just this field filled in so that it is indexed and easy to find. Note that you can include multiple topics in this field! 
- `author`: A typed link to author notes, indicating they authored the paper. Author notes are just notes with the tag `#author` and where they work. This may not seem that useful at first, but having author notes is very useful for networking! Whenever I am (re)meeting someone, I can check which of the papers I read and what I liked about them. This can also inspire useful new ideas for collaborations. I also use author notes to track where and when I met someone to reduce the amount of instances of "where did I know you from...". 
- `project`: This is a typed link to project notes for which the paper is relevant. 
- `publishedIn`: This is a typed link to a note for the journal or conference in which the paper was published. 

After that comes the main note. In this example, I summarise the paper, linking to relevant concepts discussed in the meanwhile. I also often give my opinion of the paper for future reference. 


## Topic notes (orange)
<img src="/assets/img/topic-example.png" alt="Topic note" style="width:89%; height:auto;" />

Most of my topic notes are very simple, containing at best a few sentences to describe and define the topic, preventing confusion with other topics. The most important typed link for topic notes is `subset`, which creates a [taxonomy](https://en.wikipedia.org/wiki/Taxonomy) of topics (to be more precise, a [DAG](https://en.wikipedia.org/wiki/Directed_acyclic_graph)). 
For example, the topic of reasoning shortcuts studies a specific problem within neurosymbolic learning. And this problem relates to identifiability. 
Identifiability is actually a concept note, so I am not that strict about the function of each type of note and do whatever is fast and works best.


When you use `hasTopic` from papers and talks to topic notes, they will appear automatically in the backlinks of the topic notes! 

## Concept notes (green)
<img src="/assets/img/concept-example.png" alt="Concept note" style="width:70%; height:auto;" />


Concept notes describe and define concepts. I use an exorbitant number of `aliases`, as you can see in this example: A monotone function, for example, can be monotone because it is increasing or decreasing. It is really not needed to make separate concepts for those, as these concepts are highly related and should be grouped together. 
I mainly use two types of typed links: `hasTopic` indicates the field of study that this concept is relevant for, and `isA` provides a hierarchy of concepts. In this example, monotonicity is studied within mathematics, but a monotone function is a particular type of function. 

## Project notes (red)
<img src="/assets/img/project-example.png" alt="Project note" style="width:70%; height:auto;" />

Project notes will discuss the progress of an ongoing project, or describe an idea for a new project (in which case they get the tag `#project/idea`). 
I use the `with` typed link to refer to author notes of people involved in the project. 
I also use this to indicate who I had some idea with. This saves you from going behind someones back on their own idea because you forgot where you got it from. Now you can see who I had the idea with, and who I can ask for a collaboration, help or feedback! (This might sound like a niche thing, but as you progress your career, you will thank me for this tip.)
Such notes also have the `hasTopic` typed link as usual, and I use a lot of `aliases` for rediscoverability of ideas. 




