## Summary
This repository contains Dockerfile and docker-compose.yml of [Surrogator](https://github.com/cweiske/surrogator).

## Usage
### Run
```
docker run --cap-add SYS_ADMIN --name some-surrogator -p 80:80 -d rprev/surrogator
```

### Import & Activate images
```
docker cp /path/to/imagefile some-surrogator:/opt/surrogator/raw/default.[extension]
docker cp /path/to/imagefile some-surrogator:/opt/surrogator/raw/user1@example.com.[extension]
docker cp /path/to/imagefile some-surrogator:/opt/surrogator/raw/user2@example.com.[extension]
docker cp /path/to/imagefile some-surrogator:/opt/surrogator/raw/user3@example.com.[extension]
  ...
docker exec -it some-surrogator php /opt/surrogator/surrogator.php
```
