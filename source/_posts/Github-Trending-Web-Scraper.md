---
title: Github Trending Web Scraper
date: 2016-11-09
---

# DAY 9 👾 

### I'm back 💙

#### Today I created Github Trending Repos JSON API. I've created this app to daily get updates about Github Trending Repos from 1 place rather than always checking 
[Github Trending Repos](https://github.com/trending). 

### [The JSON API can be found here](https://github.com/deadcoder0904/github-trending-json-api).

It gives repo description & the link to the repo. 

## The API is in the following format

{% vimhl js true %}
{ 
  {
    "name": "cs-video-courses",
    "url": "https://github.com/Developer-Y/cs-video-courses",
    "description": "List of Computer Science courses with video lectures."
  },
  {
    "name": "Keyframes",
    "url": "https://github.com/facebookincubator/Keyframes",
    "description": "A library for converting Adobe AE shape based animations to a data format and play it back on Android and iOS devices."
  },
  {
    "name": "pipfile",
    "url": "https://github.com/pypa/pipfile",
    "description": "Description Not Provided"
  },
  {
    "name": "md2googleslides",
    "url": "https://github.com/googlesamples/md2googleslides",
    "description": "Generate Google Slides from markdown"
  },
  {
    "name": "easy-application",
    "url": "https://github.com/j-delaney/easy-application",
    "description": "351 software engineering companies that are easy to apply to"
  },
  {
    "name": "pix2pix",
    "url": "https://github.com/phillipi/pix2pix",
    "description": "Image-to-image translation using conditional adversarial nets"
  },
  {
    "name": "FreeCodeCamp",
    "url": "https://github.com/FreeCodeCamp/FreeCodeCamp",
    "description": "The https://FreeCodeCamp.com open source codebase and curriculum. Learn to code and help nonprofits."
  },
  {
    "name": "channels",
    "url": "https://github.com/andrew--r/channels",
    "description": "A collection of useful YouTube channels for javascript developers and web designers"
  },
  {
    "name": "react-draft-wysiwyg",
    "url": "https://github.com/jpuri/react-draft-wysiwyg",
    "description": "A Wysiwyg editor build on top of ReactJS and DraftJS. https://jpuri.github.io/react-draft-wysiwyg"
  },
  {
    "name": "katana-swift",
    "url": "https://github.com/BendingSpoons/katana-swift",
    "description": "Swift Apps in a Swoosh! A modern framework for creating iOS apps, inspired by React/Redux."
  },
  {
    "name": "BeeHive",
    "url": "https://github.com/alibaba/BeeHive",
    "description": " BeeHive is a solution for iOS Application module programs, it absorbed the Spring Framework API service concept to avoid to coupling between modules."
  },
  {
    "name": "ArcLayout",
    "url": "https://github.com/florent37/ArcLayout",
    "description": "With Arc Layout explore new styles and approaches on material design"
  },
  {
    "name": "jstraining",
    "url": "https://github.com/ruanyf/jstraining",
    "description": "全栈工程师培训材料"
  },
  {
    "name": "faust",
    "url": "https://github.com/grame-cncm/faust",
    "description": "Description Not Provided"
  },
  {
    "name": "go-audit",
    "url": "https://github.com/slackhq/go-audit",
    "description": "go-audit is an alternative to the auditd daemon that ships with many distros"
  },
  {
    "name": "awesome-mac",
    "url": "https://github.com/jaywcjlove/awesome-mac",
    "description": " This repo is a collection of awesome Mac applications and tools for developers and designers."
  },
  {
    "name": "ENViews",
    "url": "https://github.com/codeestX/ENViews",
    "description": "A cool dynamic view library"
  },
  {
    "name": "Diff.swift",
    "url": "https://github.com/wokalski/Diff.swift",
    "description": "The fastest Diff and patch library in Swift. Includes UICollectionView/UITableView utils."
  },
  {
    "name": "poisontap",
    "url": "https://github.com/samyk/poisontap",
    "description": "Exploits locked/password protected computers over USB, drops persistent WebSocket-based backdoor, exposes internal router, and siphons cookies using Raspberry Pi Zero & Node.js."
  },
  {
    "name": "vue",
    "url": "https://github.com/vuejs/vue",
    "description": "Simple yet powerful library for building modern web interfaces."
  },
  {
    "name": "Eve",
    "url": "https://github.com/witheve/Eve",
    "description": "Better tools for thought"
  },
  {
    "name": "tensorflow",
    "url": "https://github.com/tensorflow/tensorflow",
    "description": "Computation using data flow graphs for scalable machine learning"
  },
  {
    "name": "Crescento",
    "url": "https://github.com/developer-shivam/Crescento",
    "description": "Add curve at bottom of image views and relative layouts."
  },
  {
    "name": "superset",
    "url": "https://github.com/airbnb/superset",
    "description": "Superset is a data exploration platform designed to be visual, intuitive, and interactive"
  },
  {
    "name": "LolliPin",
    "url": "https://github.com/OrangeGangsters/LolliPin",
    "description": "A Material design Android pincode library. Supports Fingerprint."
  }
]

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

## Voila, we have scraped the web together. It has many more applications further. We can login to Facebook & Twitter using Nightmare. We can send Automated Emails using Nightmare & many more things....

###### ⚠ Warning : It scrapes the [Github Trending Site](https://github.com/trending) which means that if the sites layout changes this project won't work

### Till the next time 👻