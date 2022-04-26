---
title: "December 2021 Roundup"
date: 2021-12-31
url: /news/december-2021/
description: "Safely download games, FAST."
---

Lots of things happened this month, lots. Lets get the important stuff out of the way first.

# Breaking changes suck.

Today our tracker implement client whitelisting.  

To download torrents you need to be using a client and version that is whitelisted.  
The whitelist is short and carefully picked, you can view it [here](/faq/).  

### Why?

In short, swarm security.  
The long answer is the amount of traffic we see is above what we should be seeing.  
This is due to several things:
1. Illegitimate clients that don't upload.
2. "People" sharing torrents outside of `rpdl.net` and `f95zone.to`  

As we create the torrents and our users upload to each other, there's a responsibility on me to protect the swarm. Everyone is super good at seeding releases, far better than I had expected so I want to be sure that when you guys leave your computer running to seed torrents that you're seeding to legitimate users.

It's a breaking change. That means a whole bunch of people are going to have issues and that's _fine_. We'll get past it and things will be better in the longterm, promise. This whitelist is the _baseline_ also, for example when qBittorrent releases a new version I'm not going to force you to update your client - you'll still be able to use 4.3.9, but you'll also have the option of using 4.4.0.
This also allows me to remove harmful clients, such as those with ads, coin-miners and ultimately, everyone will have a better and faster torrenting experience.

### Will you whitelist X client?

Highly unlikely, we spent a month testing in advance. The clients we ended up at satisfied these main criteria:

1. Open source
2. No advertisements
3. No coin-miners or malware
4. Free - no hidden charges.

`Deluge 1.3.15` is a legacy client but whitelisted as Deluge still hasn't made the `2.0` branch available on windows.
`utorrent 2.2.1` is a legacy client but whitelisted because a lot of torrent veterans still use it.  
Both of the above clients _will_ eventually be removed from the whitelist though!  
The whitelist is viewable on our [faq](/faq/).


# traffic

Let's get into some juicy stats.

```
node1 (build node): 120.79 TiB
node2 (dedicated): 174.35 TiB
node3 (backup/loan node): 146.59 TiB

cache1eu 70 TiB
cache2eu 62.05 TiB
cache1na 82.44 TiB
cache2na 63.75 TiB

November = 394tb
December = 710tb
```

The build node would usually be a lot higher, however I've increased the library substantially during December so it spent a lot more CPU time building new torrents instead of purely seeding.  
Node2 will be defunct come 1st January as it was a loaner machine from one of my projects.  
Node3 will continue to be a loaner machine from me and act primarily as an archive backup.  

I'm super happy with the performance of the cache nodes as they only came online on the 12th December and they've ~160gb NVME so there's a lot of torrent swapping.  
They've made a big difference and I couldn't be happier - big plus.

# rpdl.net

Visits and pageviews vary wildly, on days with a lot of releases we see upwards of 10,000 unique visitors but it usually hovers around 4,000-6,000.

Commits have skyrocketed, mainly due to me putting more time into updating archives and adding more games:

![](/images/commits-december.png)

In short, it's an increase from 300 to 450, about 15 updates a day.

# torrents

Our archive has grown from `555` torrents, to `763`, a little under 50% increase.  
[Being a DIK](/games/beingadik) again takes the crown for most bandwidth transferred, to the surprise of nobody!

# discord

We had some pretty bad issues with bots, so I implemented a captcha bot and had everyone verify. This has resulted in the number of people remaining the same (~300) but now with no bots, hurray!  
There's been a few new channels, admittedly mostly for me to solicit help when needed but nothing super interesting. Also, if you're a developer and want the Developer role on discord, please [let me know](/discord/)!

# funding & looking forward

It's too early to tell but I think the whitelisting will have a very positive outlook on our network.  
It's the first day but we're seeing a ~35% decrease which is good. Maybe half might be legitimate users that haven't caught up yet but being able to remove 20% of traffic which we didn't want will be a nice load off our network.  

We also passed 50% funding on our [patreon](https://patreon.com/rpdl) which is really good. It's my goal for January to bump us from current levels (62euro) to 110euro to match our monthly expenses. You can get a better overview on [our donate page](/donate/).  

If we pass that goal, we'll then be looking to reinforce again with another permanent storage node, along with a dedicated build/utility node.
All things considered, it looks very healthy and I'm super happy with our progress!

## development

We will eventually be building a new site for `rpdl.net`. At the very least, we need an RSS feed but there are several parts of the site that just aren't good enough, for example the search sucks and we need to implement a full blown tagging system.
There's a small chance we sneak this in during January but it'll likely be February.

## the end of 2021

For us, 2021 has been an incredible year.  

We've built an awesome community and we're absolutely thriving. People are reaching out to help in all kinds of ways, it's amazing. And the funding during December was great too, all in all it's been a very positive month.

So as we say goodbye to December, onwards we go into January and into a new year.  

Happy New Year to all, and thanks again for joining me on this journey!
