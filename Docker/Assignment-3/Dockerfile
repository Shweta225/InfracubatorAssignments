FROM golang:alpine AS buildgolangapp
WORKDIR /go/src/app/
COPY main.go /go/src/app/
RUN go mod init
RUN go install -v ./...
RUN go build -o golangapp


FROM alpine:latest
WORKDIR /app
COPY --from=buildgolangapp /go/src/app/golangapp /app
EXPOSE 8081
CMD ["./golangapp"]