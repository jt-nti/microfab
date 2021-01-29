#
# SPDX-License-Identifier: Apache-2.0
#

.PHONY: all
all: docker

fabric:
	git clone --depth 1 https://github.com/hyperledger/fabric.git

fabric/release/linux-amd64: fabric
	cd fabric && make "release/linux-amd64"
	mkdir -p "fabric/release/linux-amd64/config"
	cp fabric/sampleconfig/*yaml "fabric/release/linux-amd64/config"

.PHONY: docker
docker: fabric/release/linux-amd64
	docker build -t unstable-microfab .

.PHONY: clean
clean:
	rm -Rf fabric
