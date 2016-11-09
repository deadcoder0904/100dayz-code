---
title: MD Desktop with Packaging
date: 2016-11-03
---

# DAY 3 👾 

### I'm back 💙

#### Today I created MD, short for MarkDown, Desktop Previewer 

### Firstly, I created the App which is very simple, screenshot provided below

## On Linux Distro, Ubuntu Gnome 16.04

![Markdown Preview](http://imgur.com/mm7QD3c.png)

### I used Electron Packager to ship it, I currently use only Linux so I've done shipping for that only

# (1) Firstly Package it for the Current OS ( Mine is Ubuntu Gnome 16.04 )

{% vimhl bash true %}
$ electron-packager --prune . MyApp
{% endvimhl %}


## Note : `prune` flag will package it without `node_modules` folder

# (2) Then I compressed the source code into 1 file using a package called [Asar](https://github.com/electron/asar)


{% vimhl bash true %}
$ asar pack MyApp-linux-x64/resources/app MyApp-linux-x64/resources/app.asar
{% endvimhl %}

# (3) Then I deleted the original source code folder

{% vimhl bash true %}
$ rm -rf MyApp-linux-x64/resources/app
{% endvimhl %}

# (4) Then I can start the Application by simply Double Clicking It

[Final Application Here](https://github.com/deadcoder0904/electron-md-preview)

### External Resources

[Packaging and Distributing Electron Desktop Apps](https://www.youtube.com/watch?v=dz5SnmBzBXc)

### Till the next time 👻