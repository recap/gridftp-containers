#.PHONY: build

VERSION=v0.1
USAGE='make run MOUNT="/tmp/:/tmp/" SRC="file:///[PATH]" DST="ftp://[HOST]:[PORT][PATH]"'

build:
	docker build -t recap/gridftp-client:$(VERSION) .

run: build
ifndef SRC
	$(error SRC is not set, usage: $(USAGE))
endif
ifndef DST
	$(error DST is not set, usage: $(USAGE))
endif
ifndef MOUNT
	$(error MOUNT is not set, usage: $(USAGE))
endif
	docker run --net=host  -v $(MOUNT) -e SRC=$(SRC) -e DST=$(DST) recap/gridftp-client:$(VERSION)

