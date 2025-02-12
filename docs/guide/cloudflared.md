# cloudflared

## Installation

```bash
tee docker-compose.yml <<EOF
# docs: https://hub.docker.com/r/cloudflare/cloudflared
# source code: https://github.com/cloudflare/cloudflared
services:
  cloudflared:
    image: cloudflare/cloudflared
    restart: unless-stopped
    command: tunnel --no-autoupdate run --token <TOKEN>

EOF
```
