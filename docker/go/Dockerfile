FROM golang:1.17.1-alpine3.13 as builder

WORKDIR /go/src/github.com/bmf-san/go-clean-architecture-web-application-boilerplate/app

RUN apk add --no-cache git \
    binutils-gold \
    curl \
    g++ \
    gcc \
    gnupg \
    libgcc \
    linux-headers \
    make
RUN go get github.com/go-sql-driver/mysql
RUN GO111MODULE=off go get github.com/oxequa/realize
RUN go get -u github.com/go-chi/chi

CMD realize start
