FROM golang:alpine
WORKDIR /golangApp
COPY . /golangApp 
RUN go build -o main .
EXPOSE 8080
CMD ["go", "run", "main.go"]