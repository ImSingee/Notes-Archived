---
title: Poll(2) - Linux Manual Page (highlights)
---

- Author:: [[man7.org]]

- Full Title:: Poll(2) - Linux Manual Page

- Category:: #articles

- URL:: https://man7.org/linux/man-pages/man2/poll.2.html

- Highlights first synced by #Readwise [[July 4th, 2021]]
	 - The field fd contains a file descriptor for an open file.  If
       this field is negative, then the corresponding events field is
       ignored and the revents field returns zero.

	 - On success, poll() returns a nonnegative value which is the
       number of elements in the pollfds whose revents fields have been
       set to a nonzero value (indicating an event or an error).  A
       return value of zero indicates that the system call timed out
       before any file descriptors became read.

	 - poll() can fail with the error EAGAIN
       if the system fails to allocate kernel-internal resources
