FROM debian

RUN apt-get -y update && apt-get -y upgrade && \
	apt-get -y install golang-go git sqlite3

RUN	export GOPATH=/root/go && \
	mkdir -p /root/go/src/github.com/gogits && \
	cd /root/go/src/github.com/gogits && \
	git clone --depth=1 -b develop https://github.com/gogits/gogs && \
	cd gogs && \
	go build -tags "sqlite"

ENV USER="root"
WORKDIR /root/go/src/github.com/gogits/gogs
EXPOSE 3000
CMD ["./gogs", "web"]
