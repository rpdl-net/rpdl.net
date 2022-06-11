---
title: "Network Plans!"
date: 2021-10-26
url: /news/networkplans/
description: "Safely download games, FAST."
---

After much thought and testing, we've decided to change our network plans. Previously, we had planned on a clustered setup - one large node per region servicing several frontend nodes on 1Gbit/s or 10Gbit/s ports. This works well for filehosts but it doesn't really fit Bittorrent. Bittorrent doesn't need to be complicated.  

The real strengths of Bittorrent is its resiliency and how traffic/load is spread amongst active peers. If we take [nopy.to](https://nopy.to) as an example, they leverage 10Gbit/s servers to cache busy files. This is great for the end user as they get served quickly but it forces nopy to rely on expensive servers to keep up with demand.  

When downloading with Bittorrent, you download from a group of peers at once. While you will get the best speeds from the nearest peer to you, ultimately it's a combination of multiple peers working together to saturate your download speed. If a node in our swarm happened to go offline for whatever reason, the drop in capacity would be negligible - the files are just sourced from another peer.  

We're going to strategically locate 1Gbit/s servers where demand resides and add more and more servers as funding allows. This allows us to grow our footprint. As our locations improve, the swarm improves and more and more bandwidth is added to the pool. These nodes are backed with 4 terabyte of storage each - as of the time of posting we use 20% of that so there's plenty of room for growth.  

1. Our first official node will be in Texas, North America.  
2. At €100, we add a node in Amsterdam to primarily serve Europe.
3. Upon reaching €200, we double up our nodes. Two in Amsterdam for Europe and a second in California - North America. This gives us a solid backbone to grow from.
4. Our next goal is at €500, it significantly expands our global footprint. We aim to add nodes in Russia, Australia, Singapore, India and Brazil.  

Anything beyond this point will be reinforcing our existing locations, most likely adding more nodes to Europe and North America to keep up with demand.  

If you like what we do please take a moment to check out [our donation page](/https://rpdl.net/donate) and consider joining us on this journey!  
We'll post an update on Halloween to round up a very busy month and share a bunch of statistics.  
