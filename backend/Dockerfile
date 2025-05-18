FROM golang:1.22.2-alpine AS builder
RUN apk update && apk add --no-cache git
ENV GOPATH=/

WORKDIR /app
COPY go.mod go.sum ./
RUN go mod download

COPY . .
ENV CGO_ENABLED=0
RUN go build -v -o /app/todolist-app .

# Final image
FROM alpine:latest
RUN apk add --no-cache ca-certificates tzdata

WORKDIR /app
COPY --from=builder /app/todolist-app /app/
COPY --from=builder /app/migrations ./migrations
COPY --from=builder /app/.env /app/

EXPOSE 8080
CMD ["./todolist-app"]
