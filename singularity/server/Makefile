#.PHONY: build

FILE=gridftp-server_amd64.simg

build:
ifeq ("$(wildcard $(FILE))","")
	sudo singularity build $(FILE) Singularity
endif

clean: 
	rm -rf $(FILE)

run: build
	cp ../../gridftp.conf ./
	singularity run gridftp-server_amd64.simg globus-gridftp-server -c gridftp.conf
