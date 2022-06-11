---
title: "2022 - First Quarter"
date: 2022-04-05T00:05:00
url: /news/2022-first-quarter/
description: "Safely download games, FAST."
---

Grab a beer and settle down because this is a big one, some might call it a chungus.  

Here are some anchors so you can skip right to the parts you're interested in.  
[Servers](#servers), [F95zone](#f95zone), [Tools](#tools), [Games](#games), [Growth](#growth), [Developers](#developers), [Funding](#funding), [Survey](#survey), [Note](#note)
# Security and Privacy  {#security}

## Cloudflare

We've successfully moved *ALL* services off Cloudflare. There's no middle-man anymore, your connection is direct from your browser straight to our servers. Once you hit our servers, you stay there.  

## Scans and reports

`rpdl.net:` Everything is served locally _except_ some JS from Stripe on our [Donate](https://rpdl.net/donate/) page.  
[Mozilla Observatory](https://observatory.mozilla.org/analyze/rpdl.net?third-party=false) - [rpdl.net SSL](https://www.ssllabs.com/ssltest/analyze.html?d=rpdl.net&hideResults=on) - [www.rpdl.net SSL](https://www.ssllabs.com/ssltest/analyze.html?d=www.rpdl.net&hideResults=on&latest) - [Security Headers](https://securityheaders.com/?q=rpdl.net&hide=on&followRedirects=on)

`dl.rpdl.net:` This one is a little tricker so I had to allow one instance of `unsafe-eval`.  
[Mozilla Observatory](https://observatory.mozilla.org/analyze/dl.rpdl.net?third-party=false)
[dl.rpdl.net SSL](https://www.ssllabs.com/ssltest/analyze.html?d=dl.rpdl.net&hideResults=on&latest)
[Security Headers](https://securityheaders.com/?q=dl.rpdl.net&hide=on&followRedirects=on)

`tracker.rpdl.net:` This only serves torrent clients so SSL alone is fine.  
[tracker.rpdl.net SSL](https://www.ssllabs.com/ssltest/analyze.html?d=tracker.rpdl.net&hideResults=on&latest)

## Logs

We use [Nginx](https://nginx.org/en/) for our webservers and proxies. `access_log off` is specified in both the main `nginx.conf` and in the site config for _all_ sites. We don't know who's visiting, we don't want to know.  
We do track error-logs and this _does_ contain IP Addresses. This log rotates every 24 hours and we only keep 1 log. In short, if you encounter an error your IP address is logged for 24 hours in case we need to fix any issues.  

The database for `dl.rpdl.net` does not track your IP address.  
The only information we hold is your `username` and your `password` (salted and hashed).  
Whether you provide a legitimate email address or dummy data, we replace all email data with a random 10character string hourly. In the future we hope to remove it entirely.

# Servers {#servers}

There's been a few changes when it comes to hardware. On the 8th of April we're deprecating our old storage node `seed1.eu-central.rpdl.net` and we have replaced this with a new 40TB server.  
This is ~20TB usable with RAID10. All the data is transferred and it's already in rotation.  

Our next funding goal is adding a second 40TB server in EU for redundancy. After that, we'll be adding a storage server in NA to serve our cache nodes there.

Here's how it looks now:

```
EU
  20TB RAID10 storage 1Gbit/s 
  160gb NVME-RAID10 cache 1Gbit/s 
  160gb NVME-RAID10 cache 1Gbit/s 
NA
  160gb NVME-RAID10 cache 1Gbit/s
  160gb NVME-RAID10 cache 1Gbit/s
```

Here's how I hope it will look in a few weeks:

```
EU
  20TB RAID10 storage 1Gbit/s
  20TB RAID10 storage 1Gbit/s
  160GB NVME-RAID10 cache 1Gbit/s 
  160GB NVME-RAID10 cache 1Gbit/s 
NA
  20TB RAID10 storage server 1Gbit/s
  20TB RAID10 storage server 1Gbit/s
  160GB NVME-RAID10 cache server 1Gbit/s
  160GB NVME-RAID10 cache server 1Gbit/s
```

We currently archive `1,267` torrents at a size of `2.67TB`. Including work in progress, it's around `5-6TB`.  

In less good news, if you watch #general you'll be aware of the amount of hardware issues we've had in the last 2-3 weeks. The tally is _FIVE_ failures, which is an absurd anomaly.  
From RAID failures, to dead hard drives it's been very eventful. No dataloss :)

# F95zone {#f95zone}

The elephant in the room! As you're probably aware, we're still awaiting verdict from F95zone admins.  
I'm pretty confident we'll reach a happy middle ground for a few reasons:
1. Our goals. We dump all donations back into improving our network and I try be as open as I can when it comes to how we're spending our money.
2. How we operate and future plans and goals. I communicated to them (F95zone admins) weeks in advance about my concerns with leaking users IP addresses to public swarms and due to the nature of bittorrent, it's not fixable without taking the site semi-private (which we've done).
3. Userdata. See [Security](#security)
4. Torrents are _easily_ the best method of transferring data. I like to think we're doing a good job!

They might say yes, they might say no, they might ask us to make some changes.  
Whatever happens I'll keep people in the loop on [Discord](/discord)

# Tools {#tools}

We've had a few community members step up to the plate and design and host some third party tools!  
I've setup an [index](https://rpdl.net/tools/) for them, be sure to check them out.

# Branching out from Ren'Py {#games}

For the last few weeks/months we've begun archiving nearly all game engines.  
Typically anything with over 100k views we make a torrent for and at the time of writing we have ~1,300 torrents. ~1,000 of those are Ren'Py, the remaining ~300 are other game engines.  
You can check it out in the sidebar [here](https://dl.rpdl.net/torrents/recent)

# Growth {#growth}

User statistics will be a little harder to gauge now that we're no longer with Cloudflare.  
Right now, we have ~6,500 registered accounts but I don't think this is an accurate way of measuring. I think the real number of active users is somewhere between 2,000 to 3,000.  
If we return to posting links to F95zone, we should see this accelerate even faster again.  
Our [Discord](/discord) is on the way to 1,000 users too, sitting at 902 currently!

# Game Developers {#developers}

Some people wonder how we get some releases faster than other sites and most of that is down to developers giving us builds to distribute for them, it's mutually beneficial.  
If you are a game developer, feel free to hop on [Discord](/discord) or [email me](https://rpdl.net/contact/), we'd love to work with you!  

We haven't had any changes to our no-movement list, this is something we'll always honour.  
If your game is here and you don't want it here, just [let us know](https://rpdl.net/contact/)

# Funding {#funding}

The one topic I truly dislike discussing, but it's a necessary evil so here goes.  
Our funding at the moment is good but we're always looking to expand. One aspect to our current funding model that is a cause for concern is we're extremely reliant on 3-4 generous donors. I would _much_ prefer to be reliant on the many instead of the few but this is just how it is for now.  

[If you wanna join the cool kids club.](https://rpdl.net/donate/)  

PS: We still don't have advertisements and never will.  
PPPS: We also added a $1 donation tier because I've no idea why we didn't have one before.  

# The Survey {#survey}

Here are the results:
Note: When I say a feature is planned or being worked on, please don't take it to mean we'll have it in a week, or 3 weeks. We don't control development, and it's a good thing too. If you can code in rust and are interested in helping open source projects please let me know!

> How do you feel about the move to private torrents?

![](/images/question1.png)

The answers are as I expected really. As a note, I know there are a few people from a few certain websites that can't profit from our torrents anymore so take the results with a pinch of salt.  

> How do you feel about the software behind dl.rpdl.net - what's the feature you'd most like to see added (or removed).

I've attached this as a [text file](/question2.txt), otherwise we'd be here all day. Anyway, we've addressed some of these already (additional info, links to f95zone/patreon, RSS and [tools](https://rpdl.net/tools/) to automate).  
Some are defunct (issues with the old `rpdl.net` site).   
Some are also under development (comments, number of downloads, tags)  
To add some context also, when I was initially bridging all content to the new site I didn't include the links to f95zone or to the developers patreon. I added that functionality maybe a week or so afterwards? There are still some old games that haven't been updated which I will eventually get around to finishing.

> Are you happy with the selection of content available - would you like to see more RPGM/Unity/Unreal/All of the above - or are things fine as they are?

Dios mio, another [text file](/question3.txt)  
This is mostly indifferent I guess, with the general consensus being more content can't be a bad thing - which we went and did anyway.

> We'd like to remake certain accounts - specifically those who have signed up with real email addresses. Instead, we'd like people to use dummy-data (fake email addresses). Would it bother you much if we reset **all** accounts so you had to re-sign up?

![](/images/question4.png)

I worded this question very poorly, it's a bit loaded. That's on me so lets skip it.

> Would you like to see the client whitelist return? (IE only certain torrent clients would be allowed)

![](/images/question5.png)

Always a contentious topic this one. We'll more than likely have this functionality in the future so I'd expect it to return...maybe.

> Is there anything specifically you'd like to see us focus on? For example, expanding the archive - developing features or maybe working harder at getting games faster. (Note: if you're a patron for some developers and want to provide releases please let us know - we promise you'll remain anonymous)

Another [text dump](/question6.txt)

We can't _really_ automate things anymore than we do already, there still does need to be some human oversight for new torrents. Whether that's a good thing or a bad thing I'm not sure. I'm afraid we're not going to host or link to mods/walkthroughs either - the main reason behind this is that this project was never meant to be a one-stop-shop. For example, we don't plan on having forums. Think of it more like a sidecar to F95zone.  
We do plan to gather statistics at some point so users can keep track of the amount of data uploaded and downloaded, nerd stats. Comics and art are huge, they're too big for us really - it might change in future?  
Recruitment is very selective because we do automate a lot and there isn't really a need for more people. When we do need more help though we'll ping it in [Discord](/discord)

> Are you happy with the speeds you're seeing currently, and if not can you mention what general location you're in? IE East-Asia, South Africa etc.

![](/images/question7.png)

I truly do suck at making forms. Thankfully nearly all the replies are positive so let's move on.

> Small section for any notes/suggestions that weren't covered by the questions above. Be honest, if something sucks - tell us.

[Last one](/question8.txt)

Regarding the whitelist, lets use qbittorrent as an example. When we started we whitelisted Qbittorrent 4.3.9 as that was the current stable version. When 4.4.0 released, we whitelisted that too but _we did not_ remove 4.3.9 from the whitelist. Upgrading can be a pain and the whitelist was/is already a touchy topic so we've no plans to make it even more awkward...if it does return that is.  
`I'm a bad boy` Whoever submitted this, thanks for the laughs, smartass.  
There's a few suggestions too about temp email addresses, we've instead gone a different route and just straight dump any email addresses people sign up with. They're not necessary for the site (we don't do password resets) so it goes in the bin.
Double zipped archives were fixed also - hilariously while typing this up I just noticed it happend to @cake as he uploaded a new one haha.  
`preferring the torrents on f95 rather than going private` - I get it. The best way to summarise my feelings on this is like so:
One of my initial goals when setting this whole thing up was to make it like a service where my servers take the brunt of _all downloads_ - I used to advise people not to seed as a way to justify donations. With hindsight, I didn't really expect a community to form like this and it turns out a bunch of people wanted to seed the torrents regardless. I obviously warmed to this, it's awesome. Now, where I drew the line is where those peoples bandwidth (and my servers) were seeding torrents for completely third party sites. Sites that would re-upload the torrent and then spam their users with advertisements. I found this completely unacceptable. If our users are going out of their way to do something nice, the very least I can do is ensure they're not getting abused at the same time.  
`The Website seems a little bit Boring.` haha. Yeah, it kinda does! Not realy sure what we could change though - If you have suggestions let me know.  
`If an entry has multiple torrents (eg: "Season 1" and "Season 2")` Something like this is planned.  
`discord is fun to talk` It really is! It's matured a lot over the last 2 months and now there's usually people chatting at all hours, it's awesome!

# ~Fin?

That's mostly everything for now. I have a bunch of stuff in the works so here's a sneak peek:
1. A large dump of ~2-3TB of torrents for a certain flash game.
2. A dynamic stats page showing server usage (this is actually a really common request)
3. Bunch more features and updates to `dl.rpdl.net`

## One quick word from me {#note}

I want to say a special thanks to @cake for stepping up, they've added a bunch of neat donor perks and they're doing some pretty nutty things with 10g servers. I honestly won't be that surprised if they start pushing more data than this project does.  
Special thanks too to @miraclemike who's been my go-to for I guess, sanity checks? Thanks so much.  
Huge thanks to all our donors too who make this entire thing possible, you are the real MVPs.

Even if it's just $1 a month, every little helps. Just ~70 patrons at the lowest tier affords us another huge 40TB server with a 1Gbit/s uplink. It mightn't be a lot to you but it definitely adds up so go [donate!](https://rpdl.net/donate/)

---

Why are you still reading, go download some games already.
