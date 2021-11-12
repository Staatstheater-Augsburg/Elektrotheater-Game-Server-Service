# Elektrotheater Game Server Service

A [systemd](https://systemd.io/) service for the Elektrotheater game server.


# Setup

## Create directory

```bash
mkdir -p /usr/lib/systemd/system/
mkdir -p /var/log/vollstock
chown vollstock:vollstock /var/log/vollstock
```

## Create log file

```bash
touch /var/log/vollstock/game-server.log
```

## Copy systemd unit

```bash
    cp vr-theater-server.service  /usr/lib/systemd/system
```

## Enable and start

```bash
systemctl enable vr-theater-server
systemctl start vr-theater-server
```

# Control

There is a [Flask/Python service running on the server](https://github.com/Staatstheater-Augsburg/VR-Hub-Server-Control) that you can use to control the server.