---
title: Bminor/Glibc (highlights)
---

- Author:: [[github.com]]

- Full Title:: Bminor/Glibc

- Category:: #articles

- URL:: https://github.com/bminor/glibc/blob/master/misc/sys/select.h

- Highlights first synced by #Readwise [[July 4th, 2021]]
	 - /* fd_set for select and pselect.  */
      
      
        
        typedef struct
      
      
        
          {
      
      
        
            /* XPG4.2 requires this member name.  Otherwise avoid the name
      
      
        
               from the global namespace.  */
      
      
        
        #ifdef __USE_XOPEN
      
      
        
            __fd_mask fds_bits[__FD_SETSIZE / __NFDBITS];
      
      
        
        # define __FDS_BITS(set) ((set)->fds_bits)
      
      
        
        #else
      
      
        
            __fd_mask __fds_bits[__FD_SETSIZE / __NFDBITS];
      
      
        
        # define __FDS_BITS(set) ((set)->__fds_bits)
      
      
        
        #endif
      
      
        
          } fd_set;
