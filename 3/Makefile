.NOTPARALLEL:
.PHONY: init pot rc compile

all: init compile pot rc

pot:
	rc2po res.rc -P pot/

rc:
	po2rc -t res.rc -l LANG_FRENCH po/fr/ res/fr/

compile:
	windres -o res.o res.rc

init:
	rm -rf pot res
	mkdir pot res
