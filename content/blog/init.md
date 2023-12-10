---
title: "Init"
date: 2023-12-03T17:25:19-05:00
draft: false
---

## Installing themes

Since I don't have a blog elsewhere, and don't really have anything else to blog about, I'm going to use this space to keep a build log of this site, following Matt Dodson's *colophon* on his personal site, WellShapedWords.com. 

I used my day off to bundle up and walk down to Koffee?, where I ordedred a flat white and set up to try to figure out how to download the Hextra theme. I've made several attempts at building this site, and they've all been stymied by seemlingly outdated theme documentation. The last theme I tried to get, Paige, was instructing me to import the Paige module with the following:

```
$ cd yourproject
$ cat >>hugo.toml <<EOF
[[module.imports]]
path = "github.com/willfaught/paige"
EOF
```

This didn't seem to be doing anything. This was perhaps compounded by my misunderstanding of the previous step, which asked me to use desktop git to initialize a repository on Github. I was convinced the repository had to exist on Github before this command could be issued. 

In any case, I've gone with the Hextra theme and it's working. Right off the bat, their command `hugo new site my-site --format=yaml` doesn't work. As far as I can tell, there's nothing you can do to initialize the hugo config as a .yaml file. A forum post I found gave another syntax, which I tried, and that too failed. So I just manually changed the hugo.toml file to yaml, which is what the guy in the thread says he's had to do every time. Oh well.

The newer method of installation seems to be through modules, whereas Hugo's own QuickStart doc has you cloning the theme from a Github repo and placing it in the themes folder. I seem to recall seeing something to the effect that that is an outdated method, and modules are the future. Anyhow, their installation didn't involve any `cat` stuff and it worked as they described it.

## Building pages

I spent the next hour or so with another flat white and a banana nut muffin making site pages. I wanted the homepage to look something like the one Hextra has on their site, and it looked like their card elements would get me close. I realized that I could look at their Github code to see how their own homepage was built, and after copying out their custom homepage cards, they seemed to work on my site. 

I discovered these were made with shortcodes and looked into that. They're apparently using a lot of Tailwind CSS in the already intimidating Hugo shortcodes, which are themselves a type of template, which come from Go. So it was very tempting to just keep the copied fancy cards. I figured that would be stealing, though. So I'll have to learn Tailwind and shortcodes and templates.

I toyed with the idea of an embedded contact form. Google Forms come through fine as an iFrame, but they look pretty jarring and don't match your selection of light/dark theme. So I think I'll take a page from Dodson's book and leave an email. 


