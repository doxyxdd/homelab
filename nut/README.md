# NUT

Pre-reqs:
```sh

# Server
apt install nut nut-server nut-client

# Client
apt install nut-client
```

## Server Guide

Verify that the UPS matches the ups.conf file using the following command:
```sh
nut-scanner -U
```

Setup files

```sh
sudo cp ./nut/server/nut.conf /etc/nut/nut.conf
sudo cp ./nut/server/ups.conf /etc/nut/ups.conf
sudo cp ./nut/server/upsd.conf /etc/nut/upsd.conf
export UPS_PASSWORD=REPLACE_ME
envsubst < ./nut/server/upsd.template.users > /etc/nut/upsd.users
envsubst < ./nut/server/upsmon.template.conf > /etc/nut/upsmon.conf
systemctl enable --now nut-server nut-monitor
upsc ups@localhost   # verify UPS data is readable
```

## Client Guide
