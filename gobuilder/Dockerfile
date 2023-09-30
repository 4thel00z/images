FROM golang:1.20 AS builder

LABEL maintainer="4thel00z@gmail.com" \
      version="1.0" \
      description="An image that can build any go binary and run it as a docker container"

RUN apt-get update && apt-get install -y git

ARG GITHUB_URL
ARG BINARY_NAME

RUN go install ${GITHUB_URL}@latest

FROM scratch
WORKDIR /app
COPY --from=builder /go/bin/${BINARY_NAME} /app/${BINARY_NAME}
ENTRYPOINT ["/app/${BINARY_NAME}"]
