---
title: 'Building Discovery: Part 1 - MVP'
date: 2017-11-13
---

> This story is part of a series on my process building Discovery, a cutting-edge Hacker News reader.

I decided that I needed a new side project to work on and experiment with emerging cutting-edge web technologies.

<!-- more -->
Stuff like Service Workers, HTTP2 and most other things listed in Google’s [Progressive Web App (PWA) checklist](https://developers.google.com/web/progressive-web-apps/checklist). I wanted the project to be simple enough that I wouldn’t have to spend too much time on the actual implementation, so that I could actually work on features that contribute towards a PWA.

Between a Reddit and a Hacker News client, I chose the latter as the functionality is far simpler. I also decided that I would name the project **Discovery** as in Space Shuttle Discovery — the shuttle with the [most number of orbits](https://en.wikipedia.org/wiki/List_of_Space_Shuttle_missions#Flight_statistics) around the Earth. I chose to build it as a fully client-side app built on React.

---

![](discovery-1.png)

First working prototype! I started hacking away and got a working prototype done in about a day. It fetched news items from the fantastic HackerWeb API and displayed it as a easily readable list. Once I was done with this, I had to tackle my next challenge — comments.

---

What was the best way to display comments? For instance, how would nested comments be best represented, such that it would be easy for a reader to follow a full thread of comments from the root?

![](reddit-sync.png)

![](discovery-2.png)

I took inspiration from one of my favorite “thread reader” apps — Reddit Sync on Android. Using that, I built something similar into Discovery.


---

So that’s where Discovery is now. The basic reading functionality has been built, including the comments.

If you’d like to give Discovery a shot, the latest stable version will always be found at [discovery-dev.dvrylc.com](https://discovery-dev.dvrylc.com). If you’ve got any suggestions or feedback, drop me a tweet and I’ll work on it. Stay tuned!
