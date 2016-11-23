---
title: Run Github Trending Every 3 hours and Push to Github
date: 2016-11-11
---

# DAY 11 👾 

### I'm back 💙

#### Today I created a Cron Job to run Github Trending Script Every 3 hours so that the data remains updated. 

# So what is a Cron Job ?

## `Cron` is a daemon, viz, a background process which runs at a specified time. If we want to take a backup daily then instead of doing it manually every fucking day, we write a script & provide it to `cron`, then `cron` runs the script in that specified time. What if we shut down our PC or Lappy at the specified time. Then, the script won't run instead we need to use `anacron`.

# Anacron is the cron for desktops and laptops. It does not expect the system to be running 24 x 7 like a server.

## For example, if we have to send an Email to our subscribers daily at 9 PM as a regular cron job, and if our laptop is not ON at 9 PM, the Email won't be sent.

### However, if we have the same job scheduled in anacron, we can be sure that it will be executed once the laptop is ON.

# Syntax of crontab (field description)

## The syntax is:

```
1 2 3 4 5 /path/to/command arg1 arg2
OR

1 2 3 4 5 /root/email.sh
Where,

1: Minute (0-59)
2: Hours (0-23)
3: Day (0-31)
4: Month (0-12 [12 == December])
5: Day of the week(0-7 [7 or 0 == sunday])
/path/to/command – Script or command name to schedule
Easy to remember format:

* * * * * command to be executed
- - - - -
| | | | |
| | | | ----- Day of week (0 - 7) (Sunday=0 or 7)
| | | ------- Month (1 - 12)
| | --------- Day of month (1 - 31)
| ----------- Hour (0 - 23)
------------- Minute (0 - 59)
```

# Here's my `runGithubTrending` script

{% vimhl bash true %}
$ cd 'full/path/to/github-trending'
$ yarn start
$ git add -A
$ git commit -m "Update"
$ git push origin master
{% endvimhl %}

# So, here's how we can `runGithubTrending` script every 3 hours

{% vimhl bash true %}
$ crontab -l | { cat; echo "0 */3 * * * runGithubTrending"; } | crontab -
{% endvimhl %}


### Till the next time 👻