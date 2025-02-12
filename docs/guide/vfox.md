# vfox

## Installation

```bash
# https://vfox.lhan.me/zh-hans/guides/quick-start.html
echo "deb [trusted=yes] https://apt.fury.io/versionfox/ /" | sudo tee /etc/apt/sources.list.d/versionfox.list
sudo apt update
sudo apt install --yes vfox
# Hook `vfox` to your Shell
echo 'eval "$(vfox activate bash)"' >> ~/.bashrc
# Add a plugin
vfox add nodejs
# Install a runtime
vfox install nodejs@latest
# Switch runtime
vfox use -p nodejs
```
