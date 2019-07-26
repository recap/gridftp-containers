#.PHONY: build

VERSION=v0.1

build:
	docker build -t recap/gridftp-server:$(VERSION) .

run: build
	cp ../../gridftp.conf ./
	docker run -d --network host -v $(PWD)/gridftp.conf:/etc/gridftp.conf  recap/gridftp-server:$(VERSION)
