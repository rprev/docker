## Summary
This repository contains Dockerfile and docker-compose.yml of [Hubot](https://hubot.github.com/) for [Let's Chat](https://sdelements.github.io/lets-chat/).

## Usage

### Run Let's Chat
Look [this](https://hub.docker.com/r/sdelements/lets-chat/).

### Preparation at Let's Chat
1. Register new account. (it will use by hubot)
1. Generate authentication tokens for new account. (*1)
1. Add new room.
1. Join to new room, then check room ID(see URL). (*2)

### Run
```
docker run -e "HUBOT_LCB_TOKEN=*1" -e "HUBOT_LCB_ROOMS=*2" -e "HUBOT_LCB_HOSTNAME=letschat" -e "HUBOT_LCB_PORT=8080" -d --link some-letschat:letschat rprev/hubot-letschat
```
