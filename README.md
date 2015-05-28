# Yeoman Dockerfile
## Generating files as non-root

This Docker image gets you ready to go with Yeoman the right way: all generated files are NOT owned by root, so you can edit them outside the docker.

It will attach the current directory as a volume (`/src/`) so any changes made by you or by yeoman are instantly available for both of you.

### Dependencies

* [stackbrew/ubuntu:13.10](https://index.docker.io/u/stackbrew/ubuntu/)


### Installation

1. Install [Docker](https://www.docker.io/).

2. Download [trusted build](https://index.docker.io/u/felippenardi/yo/) from public [Docker Registry](https://index.docker.io/): `docker pull felippenardi/yo`

### Usage

    docker run -i -t --rm --net="host" -v `pwd`:/src felippenardi/yo
