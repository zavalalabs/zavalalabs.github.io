---
layout: post
title: Obsidian A Journey
categories: [Obsidian, Note Taking, Productivity, Tools]
---

# Background
In 2019, I found myself facing an issue with the future of my note-taking system. In my past note-taking adventures, I relied heavily on Microsoft OneNote and physical lab/engineering notebooks from Bookfactory. But in the modern day, the evolution of working from home and changes to my daily work created a gap. Not every organization utilizes the same software stack when it comes to office productivity software. Years ago you had to choose from various software like Microsoft Office, LibreOffice, Notepad, or even Lotus Notes.

![History of My Note-Taking](/images/Drawing2024-04-01.png)


> Q: Do you need a special application to take notes? 

> A: No! Any text editing application can be a note taking tool. 



  
# The Future

##  Struggles With Obsidian

My struggles with the application may not be the same as yours. I ended up running into some, what seems basic, issues which have solutions burried too deep in manuals for add-ons or worese required doing some digging with google. (That can create its own issues, can anyone say reabbit holes?)
So lets dive in on my first painpoint : 

## Daily Notes Setup
Any note-taking system you use always has some kind of phlosopy about how to do things. I will not tell you this is the **ONLY* way to do something. This methoud just fits my needs for a Day to Day accouting of what I needed. 

My workflows: 
1. A Note for every day
2. Create a file structure Matching Year -> Month -> Day
3. Automated!

### Solution

#### Formatting and Structure
Addressing my first issue "A Note for every day", EASY! Use the the built in ==Daily notes== *Core Plugin*. 
  
```json
  "format": "YYYY/MM-MMMM/MM-DD-YYYY",
  "template": "My Note Templates/Daily-Notes-Template",
  "autorun": false,
  "folder": "Daily Notes"
```