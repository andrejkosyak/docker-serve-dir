![License MIT](https://img.shields.io/badge/license-MIT-blue.svg) [![](https://img.shields.io/docker/pulls/andrejkosyak/docker-serve-dir.svg)](https://hub.docker.com/r/andrejkosyak/docker-serve-dir 'DockerHub')


This image allows you to serve static files. It's a NodeJS server application, that uses [express](https://github.com/expressjs/express), [serve-index](https://github.com/expressjs/serve-index) and [serve-static](https://github.com/expressjs/serve-static) libraries to allow user-friendly
file listing. If a file is being clicked - download is being forced.

## Usage

Example:

```
docker run -d \
    --name serve-dir-index \
    -p 30000:3000 \
    -v "/home/files-to-serve/:/home/serve-dir-index/" \
    -e "servePath=/home/serve-dir-index/" \
    andrejkosyak/docker-serve-dir:latest
```

## Config

**Environment (required)**
An `-e` variable should be passed for `servePath`. This would be the index folder.

**Volume (optional)**
You can map a volume or just serve from the container filesystem.
