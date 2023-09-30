# imags

## Motivation

This is a dumpyard for all my docker images.

## Projects

```
.
├── gobuilder
│   └── Dockerfile
└── README.md

1 directory, 2 files
```

### gobuilder

gobuilder is an parametrized dockerfile that can be used to turn a gobinary into a golang ( have to use because of cgo :/ ) container.


#### Usage

For example this command builds my [loggy](https://github.com/4thel00z/loggy) server in three lines:

```
export GITHUB_URL="github.com/4thel00z/loggy/...@latest"
export BINARY_NAME="loggy"
docker build --build-arg GITHUB_URL=$GITHUB_URL --build-arg BINARY_NAME=$BINARY_NAME -t $BINARY_NAME-gobuilder  https://raw.githubusercontent.com/4thel00z/images/master/gobuilder/Dockerfile
```

## License

This project is licensed under the GPL-3 license.
