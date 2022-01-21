---
title: The C10K Problem (highlights)
---

- Author:: [[kegel.com]]

- Full Title:: The C10K Problem

- Category:: #articles

- URL:: http://www.kegel.com/c10k.html

- Highlights first synced by #Readwise [[July 5th, 2021]]
	 - The name 'level triggered' comes from computer hardware
design; it's the opposite of 'edge triggered'.
Jonathon Lemon introduced the terms in his 
BSDCON 2000 paper on kqueue()

	 - An important bottleneck in this method is that read() or sendfile() 
from disk blocks if the page is not in core at the moment;
setting nonblocking mode on a disk file handle has no effect.
Same thing goes for memory-mapped disk files.
The first time a server needs disk I/O, its process blocks,
all clients must wait, and that raw nonthreaded performance goes to waste.

This is what asynchronous I/O is for

	 - One approach is to use memory-mapped files,
and if mincore() indicates I/O is needed, ask a worker to do the I/O,
and continue handling network traffic
