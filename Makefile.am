
EXTRA_DIST = reConServer_readme.txt
EXTRA_DIST += reConServer.config
EXTRA_DIST += *.wav

sbin_PROGRAMS = reConServer

dist_man_MANS = reConServer.8

reConServer_SOURCES = reConServer.cxx
reConServer_SOURCES += reConServer.hxx
reConServer_SOURCES += reConServerConfig.cxx
reConServer_SOURCES += reConServerConfig.hxx
reConServer_SOURCES += B2BCallManager.cxx
reConServer_SOURCES += B2BCallManager.hxx
reConServer_SOURCES += MyConversationManager.cxx
reConServer_SOURCES += MyConversationManager.hxx
reConServer_SOURCES += MyMessageDecorator.cxx
reConServer_SOURCES += MyMessageDecorator.hxx
reConServer_SOURCES += playback_prompt.h
reConServer_SOURCES += record_prompt.h

LDADD = -lrecon
LDADD += -lreflow
LDADD += -lsipXsdp
LDADD += -lsipXmediaProcessing
LDADD += -lsipXmedia
LDADD += -lsipXport
LDADD += -lsipXtack
LDADD += -ldum
LDADD += -lresip
LDADD += -lrutil
LDADD += -lssl -lcrypto -lpthread

BUILT_SOURCES = playback_prompt.h record_prompt.h

playback_prompt.h:
	echo "#ifndef _playback_prompt_h_" > playback_prompt.h
	echo "#define _playback_prompt_h_" >> playback_prompt.h
	xxd -i -u playback_prompt.wav >> playback_prompt.h
	sed  -i 's/_wav//g' playback_prompt.h
	echo "#endif" >> playback_prompt.h

record_prompt.h:
	echo "#ifndef _record_prompt_h_" > record_prompt.h
	echo "#define _record_prompt_h_" >> record_prompt.h
	xxd -i -u record_prompt.wav >> record_prompt.h
	sed  -i 's/_wav//g' record_prompt.h
	echo "#endif" >> record_prompt.h


