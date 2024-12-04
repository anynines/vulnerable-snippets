FROM bearer/bearer:latest as bear
FROM golang:1.23

COPY --from=bear /usr/local/bin/bearer /usr/local/bin
COPY --from=bear /usr/bin/git /usr/bin

WORKDIR /

RUN go install github.com/google/osv-scanner/cmd/osv-scanner@v1
