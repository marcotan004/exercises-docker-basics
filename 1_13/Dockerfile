FROM golang:1.16-alpine

EXPOSE 8080

ENV PORT=8080
WORKDIR /usr/src/app

COPY go.mod go.sum ./
RUN go mod download

COPY . .
RUN go build -o server

CMD ["./server"]