---
title: ScoopWhoop Quotes
date: 2017-01-03
---

# DAY 64 👾 

### I'm back 💙

#### Today I created a simple script to get the Url of ScoopWhoop images from Console.

> Download ScoopWhoop Quotes.

```js
var figure = document.querySelectorAll('.sw-media');
for (let i of figure) {
	console.log(JSON.stringify(i.children[0].src));
}

var img = document.querySelectorAll('.sw-para>img');
for (let i of img) {
	console.log(JSON.stringify(i.src));
}
```

# [Gist Available Here](https://gist.github.com/3d6f602b1034dfc86a80f89707040850)

### Till the next time 👻 