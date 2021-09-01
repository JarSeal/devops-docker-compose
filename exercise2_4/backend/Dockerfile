FROM golang:1.16-alpine

EXPOSE 8080

WORKDIR /usr/src/app

COPY . .

RUN go test ./common/common_test.go

RUN go build

ENV REQUEST_ORIGIN=http://localhost:5000
ENV REDIS_HOST=exercise2_4_redis_1

CMD ["./server"]