---
title: Open(2) - Linux Manual Page (highlights)
---

- Author:: [[man7.org]]

- Full Title:: Open(2) - Linux Manual Page

- Category:: #articles

- URL:: https://man7.org/linux/man-pages/man2/open.2.html

- Highlights first synced by #Readwise [[July 4th, 2021]]
	 - By default, the new file descriptor is set to remain open across
       an execve(2) (i.e., the FD_CLOEXEC file descriptor flag described
       in fcntl(2) is initially disabled); the O_CLOEXEC flag, described
       below, can be used to change this default.  The file offset is
       set to the beginning of the file (see lseek(2)).
