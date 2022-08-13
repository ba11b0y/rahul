---
title: "Reflections on first tech talk"
date: 2022-08-13T16:18:04+05:30
---

Giving a tech talk was no more than a far-fetched idea until I interacted with [Vincent](https://twitter.com/fishnets88) who was kind enough to sponsor a ticket for remotely held Python Pizza conference during COVID.

Quoting him from our twitter DM conversation

> You can always contribute to a 5 minute lightning talk. There's bound to be a super awesome function that you've learned that others don't know about.

Fast forward two years, I was fortunate that my workplace organised the 68th meetup of Golang Bangalore, and I managed to talk about the Go scheduler and the syscalls which a Go program makes during runtime.

![overview](/overview.png)

I learnt in detail on how the Go scheduler works and there's a great writeup by [Rakyll](https://rakyll.org/scheduler/) and discovered the beautifully documented and written Go runtime https://go.dev/src/runtime/proc.go

And not to miss the very interesting [io_uring](https://lwn.net/Articles/776703/) which is a fairly new asynchronous API for making syscalls. 
I did a fun benchmark during the talk to demonstrate how asynchronous execution at kernel level can really speed up programs which compared a program spawning goroutines to concurrently write to hundred files while the other program leveraging the `io_uring` subsystem to submit write requests as a batch and writing to the same number of files.
The latter was ~4x faster when benchmarked with https://github.com/sharkdp/hyperfine on a machine running Ubuntu kernel version 5.18.

// TODO: Update with the code used to benchmark.

Some people loved the talk, were kind enough to come to me and appreciate, which further led to  conversations around Go. It was great meeting [Balaji](https://twitter.com/poonai_) after a long time, and I again forgot to take a picture with him.

I felt very content after the talk, given the feeling of talking about something very interesting and some people loving it and appreciating it.

The talk as a PDF can be found [here](/syscalls_and_scheduler.pdf) and on [youtube](https://youtu.be/zgbedmitpyw)

Some images from the event:

![during_talk](/during_talk.jpg)
![group](/group.jpg)