---
title: Simplest GraphQL Express Server
date: 2017-02-01
---

# DAY 92 👾 

### I'm back 💙

#### Today I created Simplest GraphQL Express Server.

> Easiest GraphQL :art: example with Express & Fake JSON server :wink:

# Configuration

(1) Start Fake JSON server in 1 Terminal Window

`yarn run json:server`

(2) Start Express server in another Terminal Window

`yarn run dev`

(3) Open `http://localhost:1337/graphql` & enter the following

```
{
  user(id: "57") {
    name,
    gender,
    age
  }
}
```

# [Code](https://github.com/deadcoder0904/simplest-graphql-express-server)

### Till the next time 👻 