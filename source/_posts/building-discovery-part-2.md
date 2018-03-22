---
title: 'Building Discovery: Part 2 - Feature-completeness'
date: 2017-11-19
---

> This story is part of a series on my process building Discovery, a cutting-edge Hacker News reader.

In Part 1, I finished building the basic reading functionality, including the comments. In this part, I continue to work on refining the comment-reading experience and fixing other little edge cases.

<!-- more -->
## Collapsible comments

![](discovery-1.png)

One of the first things I wanted to implement was collapsible comments. For threads with a lot of discussion, such as this one, having all the comments expanded results in a ridiculously long page.

I’ve decided that comments below level 3 will be expanded by default so that the user can decide whether or not to continue reading a particular comment thread. Comments level 3 and above will be collapsed by default, just like in Reddit Sync on Android.

## Edge cases

![](discovery-2.png)
![](discovery-3.png)

In the MVP version, both job posts and “Ask HN” type posts did not render properly. For job posts, they weren’t posted by a specific user and therefore there was no username available for the render. There were also no points or comments for job posts. For “Ask HN” posts, they did not have outgoing links like ordinary posts.

Fixed these by adding item type checks before each render.

## Service worker

Last but most definitely not least, I switched on the service worker. Discovery was bootstrapped from create-react-app and so switching on the service worker was as simple as [importing and making the call](https://github.com/dvrylc/discovery/commit/487e0c9beedf5476d27d8f8fc2b8282e063a3451).

The service worker seems to be working well so far, caching the required assets and network calls. I’ll be testing it for a couple more days and if all goes well, we should be ready for the 1.0 release!

---

If you’d like to give Discovery a shot, the latest stable version will always be found at [discovery-dev.dvrylc.com](https://discovery-dev.dvrylc.com). If you’ve got any suggestions or feedback, drop me a tweet and I’ll work on it. Stay tuned!
