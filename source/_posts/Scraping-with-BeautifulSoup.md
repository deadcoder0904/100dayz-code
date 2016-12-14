---
title: Scraping with BeautifulSoup
date: 2016-11-26
---

# DAY 26 👾 

### I'm back 💙

#### Today I scraped the web in Python using the BeautifulSoup.

Firstly I thought of scraping it using JS as I am a JS guy. 

But, using headless browsers like PhantomJS or NightmareJS(which I've used earlier), BeautifulSoup felt easy. 

It has a very good documentation & you can implement anything using all the methods provided in the docs. 

The API is fantastic & easy to use. 

Also, the LOC are reduced. I usually don't care about the LOCs but sometimes its easy for the eyes to see the chunk in one frame.

In this project, I scrape popular AMAs which I'm going to use in my next Project `AMA Reader`, so I scraped the webpage given [here](https://github.com/sindresorhus/amas).

The following code does the job -

```python
from bs4 import BeautifulSoup
import urllib2
import pprint
import json
import re

pp = pprint.PrettyPrinter(indent=4)

print("Fetching the data....")

response = urllib2.urlopen('https://github.com/sindresorhus/amas/blob/master/readme.md')
html_doc = response.read()

soup = BeautifulSoup(html_doc, 'html.parser')

article = soup.find('article')
ul = article.find('ul')
li = ul.find_all('li')

arr = []
for item in li:
	link = item.find('a')['href']
	fullname = item.find('a').string
	username = link.split('/')[3]
	
	s = str(item)
	start = '</a>'
	end = '</li>'
	
	description = re.search('%s(.*)%s' % (start, end), s).group(1)
	obj = {
		"username": username,
		"link": link,
		"fullname": fullname,
		"description": description,
		"avatar": "https://github.com/" + username + ".png?size=200"
	}
	arr.append(obj)

print("Data Stored in `amas.json` file")

with open('amas.json', 'w') as outfile:
  json.dump(arr, outfile, indent=4, sort_keys=True, separators=(',', ':'))
```

# [Code on Github](https://github.com/deadcoder0904/scrape-amas/)

### Till the next time 👻 