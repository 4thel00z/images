FROM golang:1.20 AS builder

LABEL maintainer="4thel00z@gmail.com" \
      version="1.0" \
      description="An image that can build any go binary and run it as a docker container"

ARG GITHUB_URL
ARG BINARY_NAME

WORKDIR /app

RUN apt-get update && apt-get install -y git && go install ${GITHUB_URL} && cp "/go/bin/${BINARY_NAME}" /app/app

ENTRYPOINT ["/app/app"]
