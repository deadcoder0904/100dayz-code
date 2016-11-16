---
title: Github Random Emoji Generator
date: 2016-11-07
---

# DAY 7 👾 

### I'm back 💙

#### Today I created Github Random Emoji Generator Package. I've created this package to insert random Emoji's that are supported on Github in my each commit message. 

### [The npm package can be found here](https://npm.im/random-github-emoji/).

It gives all the Emoji's supported by Github. It uses a Github Emoji's JSON file. The file can be found [here](https://github.com/deadcoder0904/generate-random-github-emoji/blob/master/random.json). 

## Code


{% vimhl js true %}
var jsonContent = require("./random.json");

var arr = [];

for(var keys in jsonContent) {
	arr.push(keys);
}	

var n = Math.floor(Math.random() * arr.length);

var obj = {
	name: arr[n],
	emoji: jsonContent[arr[n]]
};

console.log(obj);

{% endvimhl %}

## Install


{% vimhl bash true %}

$ npm install --save random-github-emoji

{% endvimhl %}

## Usage


{% vimhl js true %}

const random = require('random-github-emoji');

random();
//=> { name: 'crocodile', emoji: '🐊' }

random();
//=> { name: 'hammer_and_pick', emoji: '⚒' }

{% endvimhl %}

[Final Application Code Here](https://github.com/deadcoder0904/generate-random-github-emoji/)

### Till the next time 👻