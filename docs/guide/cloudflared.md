# cloudflared

## Docker Compose

### compose.yaml

```yaml
name: cloudflared

services:
  cloudflared:
    image: cloudflare/cloudflared:latest
    command: tunnel --no-autoupdate run --token ${TOKEN}
    env_file: .env
    restart: unless-stopped

```

### .env

```dotenv
TOKEN="" # https://one.dash.cloudflare.com/

```
