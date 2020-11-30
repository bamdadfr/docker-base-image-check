#

<p align=center>
    docker-base-image-check
</p>

<p align=center>
    is my docker image up to date ?
</p>

## Dependencies

- docker
- git
- bash
- jq

## Run

```bash
wget https://raw.githubusercontent.com/bamdadsabbagh/docker-base-image-check/master/src/check.sh
chmod +x check.sh
```

## Details

### Arguments

```bash
# $1 is base image
# $2 is your docker image
```

### Return

```bash
# if image up to date, returns 0
# if image needs update, returns 1
```

### Example

```bash
if ./check.sh nginx:alpine registry.domain.com/path/to/image:latest; then
    echo "images are up to date"
else
    echo "image needs an update"
fi
```
