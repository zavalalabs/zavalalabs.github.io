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

My struggles with the application may not be the same as yours. I ended up running into some, what seems basic, issues that have solutions buried too deep in manuals for add-ons or worese required doing some digging with google. (That can create its own issues, can anyone say rabbit holes?)So let's dive in on my first pain point : 

## Daily Notes Setup
Any note-taking system you use always has some kind of philosophy about how to do things. I will not tell you this is the **ONLY* way to do something. This method just fits my needs for a day-to-day accounting of what I need. 

My workflows: 

1. A Note for Every Day
2. Create a file structure Matching Year -> Month -> Day
3. Automated!

### Solution

#### Formatting and Structure

Addressing my first issue "A Note for Every Day", EASY! Use the built-in **Daily notes****** in *Core Plugin*. Not so fast, however!

By Default your settings in this Core Plugin, may give you a headache first thing. Before you take your first note Launch settings, and set up your "Vault". 

> Just remember your *Vault* is just a file system under the Obsidian interface, think of it as your working directory

In the default settings for **Daily Notes**, each file  /note will be created in the root (top level) of your "Vault". 
Examples: (For the below table we are assuming today's date for the files April 27th 2024)
| Example                                           | Input          | Folder Structure Result (/Folder/Folder/File) | Resulting Note Title |
| ------------------------------------------------- | -------------- | ------------------------------------------------ | -------------------- |
| Year, Month(Number), Day(Number)                  | YYYY/MM/DD     | /2024/ 04/27                                     | 27                   |
| Year, Month(April),Day(Number)                    | YYYY/MMMM/DD   | /2024/April/27                                   | 27                   |
| Year, Month(Number),Day(Day of Week Abbreviated), | YYYY/MM/DD-ddd | /2024/04/27-Sat                                  | 27-Sat               |
| Year, Month(Num-Abriv),Day(Numer)                 | YYYY/MM-MMM/DD | /2024/04-Apr/27                                  |                      |

![Daily Notes Settings pane](/images/2024-04-27-ODNSettings.png)

```json
  "format": "YYYY/MM-MMMM/MM-DD-YYYY",
  "template": "My Note Templates/Daily-Notes-Template",
  "autorun": false,
  "folder": "Daily Notes"
```