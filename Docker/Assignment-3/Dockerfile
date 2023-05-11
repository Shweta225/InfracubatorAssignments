FROM golang:alpine AS buildgolangapp
WORKDIR /app
COPY . /app/
RUN go install -v ./...
RUN go build -o golangapp


FROM alpine:latest
WORKDIR /app
COPY --from=buildgolangapp /app/golangapp /app
EXPOSE 8081
CMD ["./golangapp"]
