---
title: 'Building Discovery: Part 3 - Almost there'
date: 2018-03-22 14:45:47
---

> This story is part of a series on my process building Discovery, a cutting-edge Hacker News reader.

It’s been a while since I last posted and I’ve been hard at work on Discovery, trying to make the experience something that I would gladly use as a daily Hacker News reader.

<!-- more -->
I’ll write about what has changed since the last post and give a peek into what’s to come next.

## Bugs and UX

The first thing that I’d like to cover would be the overall user experience. I mean, it was _alright_ but it wasn’t anything to write home about. Quite a few improvements have been made and I wanted to list out the bugs that have been squashed but I figured that [this](https://github.com/dvrylc/discovery/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aclosed+label%3Abug) will do.

And now for the UX improvements.

Firstly, I’ve reworked the way data is fetched into the app. A new data layer has been implemented in [these](https://github.com/dvrylc/discovery/commit/0eb44ef4c996efde84275706988264254a98787f) [two](https://github.com/dvrylc/discovery/commit/dd9997296854848f7af352911de34ee8b2c4ef31) commits and [this issue](https://github.com/dvrylc/discovery/issues/10). As a result, the reader’s scroll position is now preserved when navigating back and forth within the app.

This was an interesting UX issue to solve and I’m glad I managed to fix it cause the last thing you want is to lose your scroll position in a deep comment tree because you accidentally hit the back button (_yes_, it happened to me).

Other UX improvements include a new color scheme that's much easier on the eyes.

## Comments

![](discovery-1.png)

As we all know, comments are a _huge_ part of Hacker News and some would even argue that the comments are more valuable than the article itself.

And because of this, I set out to build a comment reader that would do these valuable comments justice. I’m glad to say that I’m pretty happy with the current state!

It’s _almost_ complete and includes features like:
* Nested comments
* Comment folding that works the right way, collapsing nested children along with it
* A nice line indicator on the left of nested comments so the reader doesn’t get lost in deep comment trees

I still think that the comment-collapsing experience needs some refinement but I can't specifically pin point the problem. Hopefully I'll get to the bottom of it.

---

So that’s what I’ve been busy with, fixing little things as they come along and trying to iterate as much as possible in the hopes of creating something that I would use on a daily basis.

As always, if you’d like to give Discovery a shot, the latest stable version will always be found at [discovery-dev.dvrylc.com](https://discovery-dev.dvrylc.com). If you’ve got any suggestions or feedback, drop me a tweet and I’ll work on it. Stay tuned!
