[![doob's github stats](https://github-readme-stats.vercel.app/api?username=doob187&count_private=true)](https://profile-summary-for-github.com/user/doob187)

## You need Help 

```
https://discord.gg/A7h7bKBCVa
```

## Traefik V2 Installer 

```
cat <<EOF > /home/installer.sh
sudo $(command -v apt) update -yqq && sudo $(command -v apt) upgrade -yqq
if [[ -d "/opt/installer" ]];then
    sudo $(command -v rm) -rf /opt/installer 
    sudo git clone --quiet https://github.com/doob187/traefikv2installer.git /opt/installer
fi
if [[ ! -d "/opt/installer" ]];then
    sudo git clone --quiet https://github.com/doob187/traefikv2installer.git /opt/installer
fi
cd /opt/installer && sudo $(command -v bash) install.sh
EOF
$(command -v bash) /home/installer.sh
```
