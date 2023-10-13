FROM golang:1.18-alpine

RUN mkdir /app

RUN addgroup -S asvgroup
RUN adduser -S -D -h /app asvuser asvgroup
RUN chown -R asvuser:asvgroup /app

USER asvuser

COPY main.go /app

EXPOSE 8080
CMD go run /app/main.go