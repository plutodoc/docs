# SSH

## Config

```bash
ssh-keygen -t rsa -b 4096 -C "<your_email@example.com>"
# Linux
ssh-copy-id <USERNAME>@<HOST>

# Windows
scp $env:HOMEPATH/.ssh/id_rsa.pub <USERNAME>@<HOST>:~/id_rsa.pub.bak
## login in the remote server
mkdir ~/.ssh
cat ~/id_rsa.pub.bak | cat >> ~/.ssh/authorized_keys && rm ~/id_rsa.pub.bak
```
