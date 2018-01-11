Docker: Golang with MeCab
=========================

[Docker Hub](https://hub.docker.com/r/wondershake/golang-mecab/builds/)

```bash
docker pull wondershake/golang-mecab
```

# Example

```
FROM wondershake/golang-mecab

WORKDIR /go/src/app
ADD . /go/src/app

RUN GOOS=linux go build -a -o /app .

RUN apk del .build_deps \
  && rm -rf /go/*

CMD ["/app"]
```
