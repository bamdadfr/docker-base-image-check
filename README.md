# @bamdadsabbagh/docker-base-image-check

is my docker image up to date ?

## dependencies

- docker
- git
- bash
- jq

## download script

```bash
wget https://raw.githubusercontent.com/bamdadsabbagh/docker-base-image-check/master/src/check.sh
chmod +x check.sh
```

## readme from `src/check.sh`

```bash
#!/bin/bash
# Author: Bamdad Sabbagh <hello@bamdadsabbagh.com>

# is my docker image up to date ?
# !!! this script assumes you are already logged in to your registries

# inputs
# $1 is base image
# $2 is your docker image

# example:
# ./check.sh nginx:alpine registry.domain.com/path/to/image:latest

# if image up to date, returns 0
# if image needs update, returns 1
```

## example of local `test`

```bash
if ./check.sh nginx:alpine docker.pkg.github.com/bamdadsabbagh/bamdadsabbagh-www/bamdadsabbagh-www:latest; then
    echo "images are up to date"
else
    echo "image needs an update"
fi
```
