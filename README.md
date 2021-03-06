# Alpha

Tiny web app to help you form a genesis file

![](./alpha.png)

- no logs
- open-source
- 300 lines of code
- single file

## Requirements

Tendermint >= 0.19

## Run it on your server

```
wget https://github.com/tendermint/alpha/raw/master/alpha.go && go run alpha.go
```

If that failed with something like `cannot use pubKey ... as type`, remove
`$GOPATH/src/github.com/tendermint/go-crypto` or run it inside a Docker
container.

OR

```
docker run -it --rm -p "8080:8080" melekes/alpha
```

[Image on Docker Hub](https://hub.docker.com/r/melekes/alpha/)

## Docker

Build docker image:

```
CGO_ENABLED=0 GOOS=linux go build -ldflags "-s -w" -o alpha
docker build -t "your_account/alpha" .
```
