c4 - C in four functions - Plan 9 edition
=========================================

An exercise in minimalism. Originally written by Robert Swierczek.

Try the following:

    pcc -D_POSIX_SOURCE -FTVwo c4 c4.c
    c4 hello.c
    c4 -s hello.c
    
	Note: The following commands do not work on the modified c4.c file because
	c4 does not like (void) in function parameter lists while pcc does not like
	empty parameter lists. c4 is in the right here,	it is valid ANSI C. C4 also
	does not like initialized variables and fails if you try to supress the
	warning about the a var in main being uninitialized. However, if you feed
	c4 the original c4.c file, the following commands will run:
	
    c4 c4.c hello.c
    c4 c4.c c4.c hello.c
