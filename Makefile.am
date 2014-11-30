bin_PROGRAMS = lzss
lzss_SOURCES = lzss.c
dist_man_MANS = lzss.1
CLEANFILES = $(bin_PROGRAMS).{txt,txt.c,d,dd}

test:
	@./$(bin_PROGRAMS) --encode $(bin_PROGRAMS).c $(bin_PROGRAMS).txt && ./$(bin_PROGRAMS) --decode $(bin_PROGRAMS).txt $(bin_PROGRAMS).txt.c
	@./$(bin_PROGRAMS) --encode $(bin_PROGRAMS) $(bin_PROGRAMS).d && ./$(bin_PROGRAMS) --decode $(bin_PROGRAMS).d $(bin_PROGRAMS).dd
	@if [ -x /bin/sha1sum ] || [ -x /usr/local/bin/sha1sum ] || [ -x /usr/bin/sha1sum] ; then sha1sum $(bin_PROGRAMS).c $(bin_PROGRAMS).txt.c && sha1sum $(bin_PROGRAMS) $(bin_PROGRAMS).dd ; fi
