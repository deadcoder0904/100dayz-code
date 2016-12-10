---
title: Refined Github
date: 2016-11-22
---

# DAY 22 👾 

### I'm back 💙

#### Today I worked on an Open Source Project called [`Refined Github`](https://github.com/sindresorhus/refined-github) created by [`SindreSorhus`](https://github.com/sindresorhus).

> Refined Github is a chrome extension that simplifies the GitHub interface and adds useful features

It is made to fix many dumb annoyances we'd like to fix. So here be dragons.

It has a lot of features.

## Highlights

- [Mark issues and pull requests as unread](https://cloud.githubusercontent.com/assets/170270/18231475/bdf83e26-72e4-11e6-958f-9ce9431d80eb.png) *(They will reappear in Notifications)*
- [Linkifies branch references in pull requests](https://github.com/sindresorhus/refined-github/issues/1)
- [Linkifies issue/PR references in issue/PR titles](https://cloud.githubusercontent.com/assets/170270/13597190/bd487ec4-e549-11e5-9521-419fa284512c.png)
- [Adds a 'Releases' tab to repos](https://cloud.githubusercontent.com/assets/170270/13136797/16d3f0ea-d64f-11e5-8a45-d771c903038f.png) *(<kbd>g</kbd> <kbd>r</kbd> hotkey)*
- [Adds user avatars to Reactions](screenshot-reactions.png)
- [Adds a quick edit button to the readme](https://cloud.githubusercontent.com/assets/170270/13379292/61cd4c42-de54-11e5-8829-f4b82ba8c2bc.png)
- [Shows current filename in the sticky pull request header](https://cloud.githubusercontent.com/assets/170270/14153322/97a8e902-f6e1-11e5-8331-19e284e3e6fa.png)
- [Adds blame links for parent commits in blame view](https://github.com/sindresorhus/refined-github/issues/2#issuecomment-189141373)
- [Shows user's full name in comments](https://cloud.githubusercontent.com/assets/170270/16172068/0a67b98c-3580-11e6-92f0-6fc930ee17d1.png)
- [Improves readability of tab indented code](https://cloud.githubusercontent.com/assets/170270/14170088/d3be931e-f755-11e5-8edf-c5f864336382.png)
- [Adds a 'Copy' button to the file view](https://cloud.githubusercontent.com/assets/170270/14453865/8abeaefe-00c1-11e6-8718-9406cee1dc0d.png)
- [Adds a shortcut to quickly delete a forked repo](https://cloud.githubusercontent.com/assets/170270/13520281/b2c9335c-e211-11e5-9e36-b0f325166356.png)
- [Adds ability to collapse/expand files in a pull request diff](https://cloud.githubusercontent.com/assets/170270/13954167/40caa604-f072-11e5-89ba-3145217c4e28.png)
- [Adds option to view diffs without whitespace changes](https://cloud.githubusercontent.com/assets/170270/17603894/7b71a166-6013-11e6-81b8-22950ab8bce3.png) *(<kbd>d</kbd> <kbd>w</kbd> hotkey)*
- [Adds links to patch and diff for each commit](https://cloud.githubusercontent.com/assets/737065/13605562/22faa79e-e516-11e5-80db-2da6aa7965ac.png)
- [Differentiates merge commits from regular commits](https://cloud.githubusercontent.com/assets/170270/14101222/2fe2c24a-f5bd-11e5-8b1f-4e589917d4c4.png)
- Easier copy-pasting from diffs by making +/- signs unselectable
- Shows the reactions popover on hover instead of click
- Supports indenting with the tab key in textareas like the comment box (<kbd>Shift</kbd> <kbd>Tab</kbd> for original behavior)
- Automagically expands the news feed when you scroll down
- Hides other users starring/forking your repos from the newsfeed
- Prompts you when pressing `Cancel` on an inline comment in case it was a mistake
- Moves the dashboard organization switcher to the right column
- Adds a `Trending` link to the global navbar. *(<kbd>g</kbd> <kbd>t</kbd> hotkey)*
- Removes annoying hover effect in the repo file browser
- Removes the comment box toolbar
- Removes tooltips
- Copy canonical link to file when [the `y` hotkey](https://help.github.com/articles/getting-permanent-links-to-files/) is used

## Install

Install it from the [Chrome Web Store](https://chrome.google.com/webstore/detail/refined-github/hlepfoohegkhhmjieoechaddaejaokhf) or [manually](http://superuser.com/a/247654/6877).

I've created a tiny function on this OSS(Open Source Software). 

The function has the ability to copy a gist to Clipboard using a Copy button. 

It is a very tiny function. I needed to edit only 3 files but learnt a lot in the process as my Code Reviewer is a perfectionist & he suggested edits for every single change I made. 

This is my first big OSS Pull Request which had a lot of reviews which you can see [here](https://github.com/sindresorhus/refined-github/pull/338). Its still not merged. But, fingers crossed it will be sooner or later. I suggest anyone reading this post to contribute to OSS as you will learn more.

### Till the next time 👻 
