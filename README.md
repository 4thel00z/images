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

gobuilder is an parametrized dockerfile that can be used to turn a gobinary into a scratch container.


#### Usage

```
docker build --build-arg GITHUB_URL=$GITHUB_URL --build-arg BINARY_NAME=$BINARY_NAME -t $BINARY_NAME-gobuilder gobuilder
```

## License

This project is licensed under the GPL-3 license.
