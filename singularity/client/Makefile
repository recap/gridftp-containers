#.PHONY: build

FILE=gridftp-client_amd64.simg

build:
ifeq ("$(wildcard $(FILE))","")
	sudo singularity build $(FILE) Singularity
endif

clean: 
	rm -rf $(FILE)

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
	singularity run --bind $(MOUNT) gridftp-client_amd64.simg globus-url-copy -vb -p 10 $(SRC) $(DST)

