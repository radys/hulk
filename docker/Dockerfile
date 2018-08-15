FROM golang:1-alpine

RUN mkdir -p /var/log/hulk
RUN apk add --no-cache git \
  && go get -d -v github.com/radys/hulk \
  && go install github.com/radys/hulk \
  && rm -rf ~/go/src/github.com/radys/hulk \
  && apk del git

ENTRYPOINT ["hulk"]

CMD ["--help"]
