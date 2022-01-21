---
title: Epoll(7) - Linux Manual Page (highlights)
---

- Author:: [[man7.org]]

- Full Title:: Epoll(7) - Linux Manual Page

- Category:: #articles

- URL:: https://man7.org/linux/man-pages/man7/epoll.7.html

- Highlights first synced by #Readwise [[July 4th, 2021]]
	 - The epoll event distribution interface is able to behave both as
       edge-triggered (ET) and as level-triggered (LT).

	 - edge-triggered mode
       delivers events only when changes occur on the monitored file
       descriptor

	 - EPOLLONESHOT

	 - If multiple threads (or processes, if child processes have
       inherited the epoll file descriptor across fork(2)) are blocked
       in epoll_wait(2) waiting on the same epoll file descriptor and a
       file descriptor in the interest list that is marked for edge-
       triggered (EPOLLET) notification becomes ready, just one of the
       threads (or processes) is awoken from epoll_wait(2).  This
       provides a useful optimization for avoiding "thundering herd"
       wake-ups in some scenarios.
