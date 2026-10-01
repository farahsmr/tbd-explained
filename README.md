# Trunk Based Development

*Started writing on June 30, 2026*

It all started when I came across a talk from code.talks 2023: Ludovic Toison’s [*“Our Journey from Gitflow to Trunk Based Development”*](https://www.youtube.com/watch?v=DDkjBqlks40). What caught my attention wasn’t just trunk-based development itself, but the fact that an entire team had decided to change the way they worked around it. The more tutorials I watched and articles I read, the more intuitive the approach started to feel, almost like the opposite of the branch-heavy Git workflow most of us are introduced to first.

I’m writing this mainly for two reasons. The first is pretty simple: I learn best by explaining things. If I can’t explain something clearly to someone else, I probably don’t understand it well enough yet. The second is that trunk-based development still doesn’t seem to be that widely known. Even a few senior engineers I’ve spoken to hadn’t heard of it, which made me think that a plain-language introduction might actually be worth writing.

> **A small note:** I’m a recent CS graduate and still early in my own journey, so this is written from my current understanding rather than from the perspective of an expert. If you notice something I’ve misunderstood or explained incorrectly, feel free to let me know.

## The Bigger Picture
A common way of working with Git is using feature branches. A task gets its own branch, work happens there, and once it is finished the branch gets merged back into main.
That is also the workflow I was most familiar with, so at first trunk-based development sounded a bit strange. The main difference is really how long work stays separate.

With a long-lived feature branch, development can continue there for days or even weeks while main is changing at the same time. Meanwhile, other people are adding code, changing files, refactoring things and eventually the branch has to be merged back, but by then both sides may have changed quite a lot.

TBD tries to keep that gap small. There is still one main branch, usually main, and developers keep integrating their changes back into it instead of letting branches grow for a long time.
Branches can still exist. That part confused me at first because some explanations make trunk-based development sound like everybody has to work directly on main, which is not necessarily the case.


```text
main
 ├── feature/login-validation
 ├── fix/navbar-spacing
 └── refactor/user-service
```

The difference is that these branches are meant to be temporary. A small change is made, reviewed, merged, and then the branch is gone again.



