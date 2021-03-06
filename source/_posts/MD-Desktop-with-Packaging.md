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

I've used Electron Packager to ship it, I currently use only Linux so I've done shipping for that only

# (1) Firstly Package it for the Current OS ( Mine is Ubuntu Gnome 16.04 )

```bash
$ electron-packager --prune . MyApp
```

## Note : `prune` flag will package it without `node_modules` folder

# (2) Then I compressed the source code into 1 file using a package called [Asar](https://github.com/electron/asar)


```bash
$ asar pack MyApp-linux-x64/resources/app MyApp-linux-x64/resources/app.asar
```

# (3) Then I deleted the original source code folder

```bash
$ rm -rf MyApp-linux-x64/resources/app
```

# (4) Then I can start the Application by simply Double Clicking It

[Final Application Here](https://github.com/deadcoder0904/electron-md-preview)

## Note : If u want to Package Application to Windows, copy & paste the below code & follow from `step 2`

```bash
$ electron-packager . MD-PREVIEW --platform=win32 --arch=x64 --version=1.4.7
```

## Sometimes it gives EACCES error, so for a workaround download Electron Version 1.4.7 from the official website & copy the `.zip` file & paste it into `~/.electron` directory & it'll work like a charm.

### External Resources

[Packaging and Distributing Electron Desktop Apps](https://www.youtube.com/watch?v=dz5SnmBzBXc)

### Till the next time 👻