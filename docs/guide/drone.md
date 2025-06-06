# Drone

## Docker Compose

### compose.yaml

```yaml
name: drone

services:
  drone:
    image: drone/drone:2
    env_file: .env
    ports:
      - "80:80"
      - "443:443"
    restart: unless-stopped
    volumes:
      - ./drone:/data

  drone-runner:
    image: drone/drone-runner-docker:1
    env_file: .env
    ports:
      - "3000:3000"
    restart: unless-stopped
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock

```

### .env

```dotenv
# docs: https://docs.drone.io/server/provider/github/
# docs: https://docs.drone.io/runner/docker/installation/linux/
DRONE_GITHUB_CLIENT_ID=""     # https://github.com/settings/developers
DRONE_GITHUB_CLIENT_SECRET="" # https://github.com/settings/developers
DRONE_RPC_SECRET=""
DRONE_SERVER_HOST=""
DRONE_SERVER_PROTO="https"
DRONE_RPC_PROTO="https"
DRONE_RPC_HOST=""
DRONE_RUNNER_CAPACITY="2"
DRONE_RUNNER_NAME=""

```
