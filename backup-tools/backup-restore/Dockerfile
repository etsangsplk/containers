FROM golang

COPY . /go/src/backup-restore/

RUN set -uex; \
    cd /go/src/backup-restore; \
    export GOPATH=/go; \
    go get; \
    CGO_ENABLED=0 GOOS=linux go build -ldflags "-s" -a -installsuffix cgo -o /go/bin/backup-restore; \
    mv /go/bin/backup-restore /usr/local/sbin
