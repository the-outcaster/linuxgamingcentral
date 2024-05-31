+++
title = "Intel Optane SSD - Review-in-Progress"
date = 2022-12-01T11:49:07-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/intel_905p/full_review/cover.jpg"
tags = ["hardware review", "work in progress", "intel", "ssd"]
keywords = ["intel optane ssd", "intel", "intel optane 905p", "intel storage"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Intel was kind enough to send one of their Optane SSDs to me. Here's my thoughts on it so far.

*Note: this review is a work-in-progress! My thoughts are NOT final.*

The reason why this is a work-in-progress is, well, I've had this drive for about a month-and-a-half so far. Normally a hardware review doesn't take me any longer than two weeks once I receive the product. But I have just been *bombarded* with other things that came in: Steam Deck accessories, the Thelio, review keys for games, etc. On top of this I'm getting a customized GameCube controller tomorrow. So between having to take care of all of those, this has caused the delay of this review.

Another factor is, this drive has required a significant amount of attention. A lot of testing had to be done measuring load times, and there's *still* plenty of more testing left to do. That being said, I wanted to have at least this preview out since it will likely take another few weeks -- maybe even *months* -- until the complete, finalized review is ready.

# What Is Optane?
Intel, at one point in time, entered the SSD business with their Optane line. These SSDs come in a variety of form factors: U.2, M.2, and PCIe. There's also different "flavors": the [905p](https://www.newegg.com/intel-optane-ssd-905p-series-960gb/p/N82E16820167463) (which is the one I have, and uses U.2), the [P1600X](https://www.newegg.com/intel-optane-ssd-p1600x-118gb/p/1Z4-009F-00621) (M.2), the [900p](https://www.newegg.com/intel-optane-ssd-900p-series-280gb/p/N82E16820167437) (PCIe), and a few others. Per the [press documentation](https://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/optane-ssd-905p-product-brief.pdf):
> The Intel® Optane™ SSD 905P is designed for the most demanding storage workloads in client systems, delivering high random read/write performance coupled with low latency and industry-leading endurance. Built with Intel® Optane™ technology, a revolutionary class of non-volatile memory, the Intel® Optane™ SSD 905P is empowering professional users, content creators, and enthusiasts to extract greater platform performance.

So basically, Optane SSDs are *really* fast hard drives, at least when it comes to random read and write speeds. Intel provides a chart to give you all the numbers you could possibly want:

![Intel Optane 905p features](/images/intel_905p/features.jpg)

Sequential read/write speeds are going to be fairly similar to your typical PCIe Gen 4 NVMe SSD. Where the 905p shines, however, is the *random* read and write speeds. They are significantly faster.

Case in point: the other drive that I use, the [Plextor M9Pe M.2 1 TB NVMe](https://www.newegg.com/plextor-m9pe-1tb/p/N82E16820249114), has a sequential read and write speed of 3,200/2,100 MBps respectively, and a random read and write speed of 400k/300k IOPS. The 905p has a sequential 2,700/2,200 MBps and a random 575k/550k IOPS. A bit surprised that the latter isn't as fast when it comes to reading sequential speeds (at least, if we go by these raw numbers), but it's nearly 1.5 times faster for random reading speeds, and almost *twice* as fast for random write. It's also slightly faster when it comes to sequential write speeds.

Intel also notes that their Optane SSDs have a significantly longer life span than traditional PCIe NVMe drives. Mean time between failures (MTBF) on the 905p is 1.6 million hours. But that's not much longer than the Plextor drive, which has a MTBF of 1.5 million. In any case, I'm not expecting the 905p to "die" out anytime soon; it will likely last for a good 20 years at least.

Sadly, however, Intel is retiring these SSDs. So I'm grateful Intel sent one over, so that I could give you guys a taste of what this SSD is capable of.

# Package Contents
Here's what came in the mail when I got the drive:

![Intel Optane 905p package contents](/images/intel_905p/full_review/contents.jpg)

In the box, besides the drive itself, was a M.2 adapter, an instruction manual, and a couple of screws. I also got a personal, hand-written thank you note from Jacek Wysoczynski, the one who is "responsible for Strategy and Solution Architecture in the Intel Optane Group" and the one who I got in touch with for getting a review unit of the 905p.

![Thank you note from Jacek from Intel](/images/intel_905p/full_review/thank_you_note.jpg)

I kind of dig that. It's nice to get that "personal touch" whenever you get a package. It was also nice of him to give me the largest capacity that Intel had at the time. Initially he offered a 240 GB drive. When I told him that wasn't good enough, he went the extra mile of finding me one that's twice the size. 

The manual provides some brief instructions on how to get the drive installed on your system, be it PCIe or, in my case, U.2.

![Intel Optane 905p instruction manual](/images/intel_905p/full_review/manual.jpg)

Here's the drive underside:

![Intel Optane 905p underside](/images/intel_905p/full_review/drive_underside.jpg)

If you've never heard of U.2 before, don't worry; I never heard about it either until I got this drive. It looks very similar to the connections a mechanical hard drive would use. The exception would be, if you can see in the photo below, there's this little "notch" towards the center of the connection, and the connection is one piece, rather than having two separate connections.

![Intel Optane 905p U.2 connection](/images/intel_905p/full_review/connection.jpg)

My power supply doesn't have this type of connection (and I would tend to think most PSUs don't). Fortunately the box comes with a M.2 adapter. You connect the drive on one end, add a SATA connection with your PSU, and connect the other end to an available M.2 slot on your motherboard. Note that the drive will *not* get enough power if you don't supply the SATA connection -- my system wouldn't detect the drive otherwise.

![U.2 to M.2 adapter](/images/intel_905p/full_review/m2_adapter.jpg)

See this clip here in my desktop? That's where a 2.5" drive can go.

![2.5" drive clip in my desktop](/images/intel_905p/full_review/where_the_drive_is_supposed_to_go.jpg)

But with the 905p being a 15mm thick brick, it was too thick to fit inside the clip. I ended up having to take the clip out. I can fit the drive in now, even though it might be a little awkward since it's not wide enough to accomodate screws on both sides. I can only put one in on one side. One screw is better than none, though; at least it will hold the drive in place.

![Intel Optane 905p installed](/images/intel_905p/full_review/installed.jpg)

With the drive in place, here's the connection on one side:

![Intel Optane 905p U.2 connection](/images/intel_905p/full_review/u2_connection.jpg)

And then, the M.2 connection on the other:

![Intel Optane 905p M.2 connection](/images/intel_905p/full_review/m2_connection.jpg)

# Is Intel Optane Actually Faster?
In some ways, it definitely is. When it comes to web browsing, downloading and upgrading packages on Arch, as well as general multi-tasking, I've noticed my experience has been more "seamless." I don't expect any downtime when trying to launch an application, even with tens of them open. Arch has been super-responsive and fast.

To give you an idea of speed, as I hinted with my [first impressions](https://linuxgamingcentral.com/posts/intel-optane-905p-ssd-first-impressions/), it takes about three-and-a-half minutes to transfer 250 GB worth of games, from my Plextor drive to the 905p. That's roughly 1.2 GBps. And it takes about five minutes to get Arch installed as btrfs with the NVIDIA graphics drivers and the Cinnamon desktop included.

![Intel Optane 905p file transfer speed](/images/intel_905p/file_transfer.jpg)

Here's a more accurate comparison between the read and write times between both drives. This was benchmarked with GNOME's Disk utility:

![Intel Optane 905p vs. Plextor benchmark](/images/intel_905p/full_review/read_and_write_comparison.jpg)

That's a pretty nice jump, huh? Both read and write times are seeing significant improvements, especially with the former. Average access time on the Plextor is also *ten times* longer. The simplicity of the graph with the 905p is nice; it's not all over the place like the Plextor drive. It's a lot more "consistent."

I managed to get a full benchmark of the 905p with Phoronix Test Suite. You can see the entire results on [openbenchmarking.org](https://openbenchmarking.org/result/2211296-NE-BENCHMARK70). But here's a few highlights.

**SQLite:**

![Intel Optane 905p SQLite](/images/intel_905p/full_review/sqlite.png)

That's far faster than *any* other drive on [openbenchmarking.org](https://openbenchmarking.org/test/pts/sqlite&eval=d68053028e816d1714272131286a187def18102e#metrics). Testing 128 threads, for example, is about 50 seconds on the 905p. The closest competitor would be the [Crucial 500GB CT500P5SSD8](https://www.crucial.com/ssd/p5-plus/ct500p5pssd8), which doesn't even come close at 80 seconds!

**Flexible I/O:**

![Intel Optane 905p FIO](/images/intel_905p/full_review/fio.png)

Random read at 4 KB with the Linux AIO engine competes very closely to the Samsung SSD 970 PRO. This drive ranks 92nd percentile at an average of 347k IOPS. The 905p does a little better at 363k IOPS. Not the fastest in this instance, but it's definitely in the [top three](https://openbenchmarking.org/test/pts/fio&eval=c73b01994343242e61980368b45e90bd747f9696#metrics).

**FS-Mark:**

![Intel Optane 905p FS-Mark](/images/intel_905p/full_review/fs-mark.png)

Testing 5k files that are one MB in size with four threads -- the 905p scores 1640.8 files. This does just *slightly* worse than the [3841GB Micron 9300 MTFDHAL3T8TDP](https://www.micron.com/products/ssd/product-lines/9300), which can process 1650 files. This would rank the 905p in fourth place on [openbenchmarking.org](https://openbenchmarking.org/test/pts/fs-mark&eval=5ca205e1e391516a4179429c03238ddcd7933fb2#metrics).

The gaming aspect, however, is where I'm scratching my head. After hours of testing various games and their load times, I am simply *not* seeing any faster loading times compared to my Plextor drive. I've wiped the shader cache and compat data on both drives, ensuring that every game had a clean "slate," so to speak. I even went so far as to re-format the 905p as ext4, since apparently it's the best file system to use, according to Alka from the Optane Discord group that I'm in. Absolutely no difference in loading times.

I tested the following titles:
- *Horizon Zero Dawn*
- *Destroy All Humans 2! Reprobed*
- *Kena: Bridge of Spirits*
- *Final Fantasy VII Remake*
- *Sonic Frontiers*

All hard-hitting games, right? Big open-world environments that are definitely going to take a toll on your hard drive in terms of loading time. You can see the comparisons between my Plextor drive and the 905p below. Every game was tested at least three times. Both drives, at the time of testing, were using btrfs and using Arch Linux, using the highest available graphics settings for each game at 1080p. Unless otherwise noted, these games were tested with Proton 7.0-4 (*Horizon Zero Dawn* was tested with GE-Proton7-41, as for some reason the game loads *much* faster with this than vanilla Proton). Load times were recorded with a stopwatch, rounded to the nearest second.

![Intel Optane 905p vs. Plextor game loading times](/images/intel_905p/full_review/load_time_comparisons.png)

Definitely a head-scratcher, right? Why would *Kena* and *Sonic Frontiers* take a second longer than the Plextor drive? (Although, the recorded times are rough estimates, so take the results with a grain of salt.) Again, even after formatting the 905p as ext4, the load times were similar.

Something's definitely not sitting well here. So, despite the extensive testing I've done so far, I have yet much more troubleshooting left to do. There's just got to be *something* that I'm missing here. I don't understand why game loading times are the same, perhaps just a tad slower.

# Worth Your Time?
That remains to be determined. After all, this review is a work-in-progress. In general, yes, I would say getting an Intel Optane drive is worth it, for general use. Gaming, however, you might not see any significant difference, at least as far as loading times. But perhaps where the 905p shines in this case is when it comes to shader compilation times. In other words, when you launch a game for the first time, there's probably going to be a lot less stutter from getting shaders cached. More testing required for that.

Special thanks to Jacek from Intel for sending the drive over for my review, and for him trusting me, being the small content creator that I am. Thanks also go to Luke Short for helping me get in touch with Intel, and Alka for their benchmarks and their assistance in helping get this review out.

You can get the [905p (960 GB)](https://www.newegg.com/intel-optane-ssd-905p-series-960gb/p/N82E16820167463) on Newegg for $400. If you're looking for something less expensive, you can go for the [P1600X (118 GB)](https://www.newegg.com/intel-optane-ssd-p1600x-118gb/p/1Z4-009F-00621) for $76. You might want to hurry and grab them before they sell out, since Intel won't be producing any more!

**TL;DR**

The good:
- very fast, at least when it comes to general use

The not-so-good:
- too thick to fit inside the 2.5" drive bay that I have
- the 905p uses U.2 and requires a M.2 adapter
- game load times aren't seeing any difference compared to a regular PCIe Gen 4 SSD

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
