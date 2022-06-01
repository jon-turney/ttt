.NOTPARALLEL:
.PHONY: pot recovery rc compile

all: init compile pot recovery rc

pot:
	rc2po -P res/en/ pot/

recovery:
	rc2po -t res/en/ res/fr/ po/fr/

rc:
	po2rc -t res/en/ -l LANG_FRENCH po/fr/ res/fr/

compile:
	windres -I. -o res.o res.rc

init:
	rm -rf po pot
	mkdir po pot
