---
title: "October 2021 Roundup"
date: 2021-11-07
url: /news/october-2021/
description: "Safely download games, FAST."
---

I mentioned [here](/news/networkplans/) that I was typing up an end of month roundup but a few things happened which delayed this.  
Anyways, it's here now - just a week late - Sorry!

---

# The Bad News

[Nopy.to](https://nopy.to) has at least temporarily, ceased operations. I mentioned previously I always had a passion for pushing bandwidth, it was my chats with the person behind Nopy and the staggering amounts of bandwidth they were pushing that propelled me into making this site. I'll always measure the success of rpdl.net against what the Nopy team achieved because in my eyes, they did it perfectly.  
No ads, no limits and entirely crowdfunded and I'll do my best to follow along in their shadow.

# The Good News

It's so incredibly bittersweet. The morning I hear of the Nopy issues is the same morning we get our first patron. It's awesome to see people believing in both this site and our goals, so much so that you're willing to help fund it - it's incredibly humbling. Additionally - almost to the hour of Nopy going down - traffic on our network shot through the roof. That pushed the traffic for October to a combined 146tb.  
Considering Nopy did 16PB monthly, there's still a very long way to go!

---

# Torrents

We passed 400 torrents during October, here's the [400th release](/games/totalcorruption/)!

417 active torrents, clocking in at 861gb. The most popular torrent is [Reunion](/games/reunion/) which shifted almost 10tb by itself!  

Midway through the month I made some changes to how torrents were created and incorporated piece sizes better. Now the amount of pieces scales up and down by the size of the release, as it should have been from the start. Initially all torrents used 256kb pieces which is ridiculously small for larger torrents. The torrent file for games +10gb ends up bearing nearly half a megabyte large which is stupid - it's fixed now anyway.  

# rpdl.net
For the site itself, I moved it entirely to [Cloudflare Pages](https://pages.cloudflare.com/). I was already Cloudflare anyway so figured it'd make deployments that bit easier.  

As of now there's been 325 commits to the site too, an average of about 6-8 updates per day.  

# Servers

One thing I noticed is that while Europe is currently pretty well served, speeds to America especially are strained. I do actively need to add new servers to the pool to better service more areas. My current setup will also hit their bandwidth limits relatively soon, probably by the end of December.
I updated [our patreon](https://patreon.com/rpdl) recently to reflect this.

Bittorrent is the way forward and with the proper infrastructure in place, we could quite literally, seed ALL the Ren'Py content we can find. I'm slowly expanding our catalogue too, adding new games every day. Eventually we'll cover all Ren'Py games - hopefully by Christmas.

# Releases

There is one outstanding issue with releases working on MacOS currently, one that I'm trying to find a solution for still. When I do, I won't update my entire catalogue but instead re-package games specifically for people if requested. Obviously, all new releases afterwards will be fixed by default.  

I don't currently have an ETA for this, however there is a workaround noted [here](https://f95zone.to/threads/how-to-create-a-mac-version-of-any-renpy-game.3289/post-6852534).

---

Lastly, I want to thank again those who have chosen to help fund this project. You're awesome!  

The November update is already looking to exceed all expectations too!
