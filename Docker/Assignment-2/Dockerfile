FROM golang:alpine
WORKDIR /golangApp
COPY main.go /golangApp
RUN go build -o main .
EXPOSE 8080
CMD ["go", "run", "main.go"]