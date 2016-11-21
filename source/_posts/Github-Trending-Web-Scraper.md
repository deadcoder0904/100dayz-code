---
title: Github Trending Web Scraper
date: 2016-11-09
---

# DAY 9 👾 

### I'm back 💙

#### Today I created Github Trending Repos JSON API. I've created this app to daily get updates about Github Trending Repos from 1 place rather than always checking 
[Github Trending Repos](https://github.com/trending). 

### [The JSON API can be found here](https://github.com/deadcoder0904/github-trending-json-api).

It gives repo name & the link to the repo. 

## The API is in the following format

{% vimhl json true %}

{
  "description": [
    "List of Computer Science courses with video lectures.",
    "Generate Google Slides from markdown",
    "The https://FreeCodeCamp.com open source codebase and curriculum. Learn to code and help nonprofits.",
    "A collection of useful YouTube channels for javascript developers and web designers",
    "全栈工程师培训材料",
    "Exploits locked/password protected computers over USB, drops persistent WebSocket-based backdoor, exposes internal router, and siphons cookies using Raspberry Pi Zero & Node.js.",
    "Add curve at bottom of image views and relative layouts.",
    " This repo is a collection of awesome Mac applications and tools for developers and designers.",
    "345 software engineering companies that are easy to apply to",
    "A simple and customizable two or three states Switch View",
    "Easily generate cross platform Swift framework projects from the command line",
    "A cool dynamic view library",
    "",
    "A collection of various awesome lists for hackers, pentesters and security researchers",
    "Minimal and clean examples of machine learning algorithms",
    "Deep Learning Porn Video Classifier/Editor with Caffe",
    "Dash gives your iPad and iPhone instant offline access to 150+ API documentation sets",
    " Fast async task based Swift framework with focus on type safety, concurrency and multi threading",
    "JavaScript Scrum App to manage tasks with ease",
    "A minimalistic framework for server-rendered Vue.js applications (inspired by Next.js)",
    "",
    " Cicerone is a lightweight library that makes the navigation in an Android app easy.",
    "视频播放器，支持基本的拖动，声音、亮度调节，支持边播边缓存，支持视频本身自带rotation的旋转（90,270之类），重力旋转与手动旋转的同步支持，支持列表播放 ，直接添加控件为封面，列表全屏动画，列表小窗口支持拖动，5.0的过场效果，其他一些小动画效果。简书:",
    "inline markdown for react/jsx",
    "Simple yet powerful library for building modern web interfaces."
  ],
  "links": [
    "https://github.com/Developer-Y/cs-video-courses",
    "https://github.com/googlesamples/md2googleslides",
    "https://github.com/FreeCodeCamp/FreeCodeCamp",
    "https://github.com/andrew--r/channels",
    "https://github.com/ruanyf/jstraining",
    "https://github.com/samyk/poisontap",
    "https://github.com/developer-shivam/Crescento",
    "https://github.com/jaywcjlove/awesome-mac",
    "https://github.com/j-delaney/easy-application",
    "https://github.com/RiccardoMoro/RMSwitch",
    "https://github.com/JohnSundell/SwiftPlate",
    "https://github.com/codeestX/ENViews",
    "https://github.com/ShapeLab/SwarmUI",
    "https://github.com/Hack-with-Github/Awesome-Hacking",
    "https://github.com/rushter/MLAlgorithms",
    "https://github.com/ryanjay0/miles-deep",
    "https://github.com/Kapeli/Dash-iOS",
    "https://github.com/arikis/Overdrive",
    "https://github.com/i-break-codes/scrum-board",
    "https://github.com/nuxt/nuxt.js",
    "https://github.com/pypa/pipfile",
    "https://github.com/terrakok/Cicerone",
    "https://github.com/CarGuo/GSYVideoPlayer",
    "https://github.com/threepointone/markdown-in-js",
    "https://github.com/vuejs/vue"
  ]
}

{% endvimhl %}

This project looks very simple, but it was very tricky because it was my first time using [Nightmare JS](https://nightmarejs.org). Nightmare is a High Level Automation Library made using Electron. It is same as [Phantom JS](http://phantomjs.org/), but it is fast & a little modern.

### To scrape today's trending, follow the steps given below :-

# (1) Clone this repo

{% vimhl bash true %}
$ git clone git@github.com:deadcoder0904/github-trending-json-api.git
{% endvimhl %}

# (2) Go into the directory

{% vimhl bash true %}
$ cd github-trending-json-api
{% endvimhl %}

# (3) Type `yarn` to install all dependencies

{% vimhl bash true %}
$ yarn
{% endvimhl %}

# (4) Type `yarn start` to start scraping the web

{% vimhl bash true %}
$ yarn start
{% endvimhl %}

### In a minutes time, depending on the speed of your internet, a new file will be created according to today's date in `json` folder.

## Hurray, we have scraped the web together. It has many more applications further. We can login to Facebook & Twitter using Nightmare. We can send Automated Emails using Nightmare & many more things....

###### :warning: Warning : It scrapes the [Github Trending Site](https://github.com/trending) which means that if the sites layout changes this project won't work

### Till the next time 👻