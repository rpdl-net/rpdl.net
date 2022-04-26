---
title: "November 2021 Roundup"
date: 2021-12-01
url: /news/november-2021/
description: "Safely download games, FAST."
---

Wow, where do I even start. I guess lets get some of the raw numbers out of the way first.  
# traffic
In my [October roundup](/news/october-2021/) I noted: 

> Additionally - almost to the hour of Nopy going down - traffic on our network shot through the roof. That pushed the traffic for October to a combined 146tb.

I had planned for this to grow to between 200-250tb through November, so lets take a peek:

```
node1 112.46 TiB
node2 149.37 TiB
node3 132.77 TiB
```

So congrats, grand total is **~394tb**. A tiny bit under double what I'd originally planned for.  

Note: Only node1 is officially designated for seeding - node2 and node3 are for other projects. Additionally, node1 should have more traffic but it's also my build server so quite a lot of CPU time is used on new builds and seeding my other servers.
# rpdl.net
```
rpdl.net is doing ~3.5k pageviews daily
rpdl.net is seeing ~1k different people daily
```
The underlying codebase received just under 300 individual updates throughout November, a frankly intimidating 10 updates a day average.

![](/images/commits.png)

# torrents

As of this moment, I have 555 torrents tagged as `rpdl` with a further 16 untagged. What this means is 1.yes, today was very busy and I haven't updated them yet and 2. the actual number is probably 563.

![](/images/rpdl-torrents-november.png)

The easy winner of most bandwidth this month is [Being a DIK](/games/beingadik/). Worth noting: This game received a bugfix pretty quickly which reset it's total upload amount. It alone accounted for nearly 5% of all November traffic.

# compressed

The eagle-eyed among you may have noticed that [Techstar](https://f95zone.to/members/techstar.354589/) has started offering torrents built on and seeded via rpdl.net. This was something we had in the works for a little while and required a lot of coding and testing.  

Everything appears to be pretty stable the last few weeks and I couldn't be happier. So a big thanks to Techstar for putting up with my late night rambling and helping me troubleshoot, plus his patience while we got all this setup!

# deployment

I made a few changes to how my deployment works. It takes a little longer now but it's a lot more robust.  
There was a nasty bug with seeds not coming online which is now fixed. I've also incorporated a Discord webhook so everyone on Discord gets the torrents a few minutes early, which neatly leads to my next topic:

# discord

I caved and made a Discord, and I immediately realised I should have made one weeks earlier.  
There is _already_ 302 people idling on the discord...it's 2 weeks old..  
If you're not on it already, you can join it [here](/discord/)!

---

I really thought I'd type a lot more about all this because I was so excited to share, but that's the bones of November, neatly wrapped up. I lied, there's more;

# challenges

Today especially, November 30th was difficult. I wrote up a post on [f95zone](https://f95zone.to/threads/rpdl-net-discussion-questions-torrents.96535/page-10#post-7052183) that details a lot of the issues I face.  
The issues I concentrate on most are temporary and outside of my control - f95zone server issues and [Cloudflare issues](https://www.cloudflarestatus.com/incidents/c3nw000ynl86). These will clear up eventually so it's not a big deal.  

One issue I do face is that on busy days, my servers are routinely pinned at 100% usage. There's no way around this except adding more servers to spread the load out. I go into this a little in my post on f95zone that I linked above.  

If you do have a few bucks spare, I'd be extremely appreciative if you tossed some my way via [my patreon](https://www.patreon.com/rpdl).  

## december and looking to the future

This project is a bit like a startup, it's creaking under it's own weight and really needs a bit of investment to support itself. The traffic and growth shows we have something special here and truly, the sky is the limit. 

However, if the current growth continues my infrastructure will not be able to keep up with December. It's simply not possible without additional servers. rpdl.net *is not* going to go down or anything to that effect - instead what you'll see is larger swarms dependant on three servers which max out at 450 peers combined.  

Today at it's peak, the amount of active peers on rpdl.net torrents peaked at just over **4,000 active peers in a thirty minute period**. In October I predicted a 30% growth increase and it almost doubled. It's impossible to predict when this insane growth will stop but without your help, I don't think it'll be able to cope with its current funding levels.

To clarify, this was, is and always will be a hobby to me, one that I'm happy to spend money on - I always will. Any funding that comes in goes straight to new servers additional to the servers I already pay for myself.  

**Right now, this project needs your help to push it above and beyond.  
To keep up with December I think we'd need approximately ~150euro in monthly funding to add three (maybe 4) extra dedicated servers. Two more devoted to seeding, and a central build/sync server.**

---

Before starting this I chatted with the person behind Nopy, I was and still am in complete awe at what they achieved. One thing has become crystal clear to me though. Since Nopy has had to close it's doors more and more of it's users are starting to call rpdl.net home. It's very humbling to me, words can't describe.  

Thank you so much to everyone on Discord who's helping with spotting leaks, typos, errors and issues. Frankly there are too many of you to name. Please, keep doing what you're doing, it's a group effort and always will be - I'm just the person at the captains wheel steering it.

There's still an incredibly long way to go but I'm convinced we'll not only reach those same heights but one day, pass them too. If you want to join the 302 people and myself on Discord, [click here](/discord/) and if you feel so inclined, here's [my patreon](https://patreon.com/rpdl) again.

See, I knew I'd write up a huge essay. Anyways, with that we'll say goodbye to November and hello to December!

**LETS GOOOOOOOOOOOO** ❤️
