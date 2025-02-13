# cloudflared

## Installation

```bash
# Write docker-compose.yml
cat > docker-compose.yml <<EOF
# docs: https://hub.docker.com/r/cloudflare/cloudflared
# source code: https://github.com/cloudflare/cloudflared
services:
  cloudflared:
    image: cloudflare/cloudflared
    env_file: .env
    restart: unless-stopped
    command: tunnel --no-autoupdate run --token \${TOKEN}

EOF
# Write .env
cat > .env <<EOF
TOKEN="<TOKEN>"

EOF
```
