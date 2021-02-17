FROM golang:latest
RUN mkdir /app
ADD . /app/
WORKDIR /app
RUN go build -o ./build/main github.com/basdemir/simplego/simplefrontend/cmd/simplefrontend
CMD ["/app/build/main"]