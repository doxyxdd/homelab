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
sudo cp ./nut/nut.conf /etc/nut/nut.conf

```

## Client Guide
