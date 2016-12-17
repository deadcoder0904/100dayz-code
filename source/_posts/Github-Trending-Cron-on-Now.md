---
title: Github Trending Cron on Now
date: 2016-11-30
---

# DAY 30 👾 

### I'm back 💙

#### Today I deployed my Github Trending CronJob on [Now](https://zeit.co/now).

Now is a PAAS(Platform As A Service) provided by [Zeit](https://zeit.co/).

It provides Immutable Deploys which are free for public deploys.

Immutable Deploy means that once a service is deployed its never gonna change again.

Consider an example on How To Deploy A Simple HTML file on Zeit's Now.

```bash
$ mkdir html-example
$ cd html-example
$ touch index.html
```

```html
<!DOCTYPE html>
<html>
<head>
	<title>A2K</title>
</head>
<body>
	<h1>HELLO WORLD</h1>
</body>
</html>
```

To deploy this on Zeit's `Now` you just have to type the command `now`

For this `now` needs to be installed on your system. 

Install `now` with the following command. 

Assuming `npm` is installed on your system, if it isn't just install `node` from `https:nodejs.org`. 

NPM is a Node Package Manager that comes installed with node. It manages all Javascript Packages. 

`ProTip:-`

 Use `yarn` instead of `npm` as `yarn` is much better than `npm`. I would've gone into the details but its out of the scope of this post.

```bash
npm install now -g
```

Type `now` to deploy it.

```bash
now
```

It'll ask for `email` & `password` for the first time. Then it'll deploy & will generate a unique URL. Something like

```bash
https://html-example-78nsd82s.now.sh
```

Now change the text in `index.html` file from `HELLO WORLD` to `HELLO A2K` & deploy again using `now` command.

This time it won't ask for `email` & `password`. But as the text is changed from `HELLO WORLD` to `HELLO A2K`, it'll generate a unique URL. Something like

```bash
https://html-example-235xz245.now.sh
```

Notice the hash changes. Now if you visit the earlier URL it'll still display `HELLO WORLD` & the new URL will display `HELLO A2K`. 

Thus, Zeit's Now is the first PAAS which provides immutable deploy's. 

I used to use `Surge` & `Github Pages` for Static Files; `Heroku` & `Openshift` for Node JS Scripts.

But now I'll be using Zeit's Now. Its super easy & provides us with the SuperPower of Immutability.

I've used it in my Use Case for Github Trending about which you can read it [here](https://100dayz.js.org/2016/11/11/Run-Github-Trending-Every-3-hours-and-Push-to-Github/).

I have earlier made a CronJob for that but what if I don't keep my PC On at the particular time when Cron is going to execute then it won't run the script.

Also, with Anacron it waits till the next time you ON your PC, so if I keep my PC off for a weekend Anacron might run the script on the last day only.

That's why I need some server which runs 24x7/365 & that's why I'm using Zeit's `Now`.

I've written a Node JS script which uses Cron internally & pushes to Github everyday late night @ 3.00 am according to `LA` Timezone.

Now I can keep my PC off for the entire year & it'll still push Github Trending Repos online. 

The Code is kept closed source.

### Till the next time 👻 