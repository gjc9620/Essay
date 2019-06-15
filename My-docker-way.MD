# My-docker-way

### Docker image list
`docker ps`

### Sync timezone
`docker cp /etc/localtime d98c8a689c13:/etc/localtime`

### Access container
`docker exec -ti d98c8a689c13 /bin/sh`

### restart container
`docker restart d98c8a689c13`

### Logs
`docker logs -f d98c8a689c13`

### About V2ray
`vi /etc/v2ray/config.json`

```json
{
  "inbound": { //Don't write ip
    "port": 1080,
    "protocol": "socks",
    "settings": {
      "auth": "noauth"
    }
  },
  "outbound": {
    "protocol": "vmess",
    "settings": {
      "vnext": [
        {
          "address": "IP",
          "port": 24291,
          "users": [
            {
              "id": "ID",
              "alterId": 64
            }
          ]
        }
      ]
    },
    "streamSettings": {
      "network": "mkcp",
      "kcpSettings": {
        "mtu": 1350,
        "tti": 20,
        "uplinkCapacity": 20,
        "downlinkCapacity": 300,
        "congestion": false,
        "readBufferSize": 6,
        "writeBufferSize": 6,
        "header": {
          "type": "dtls"
        }
      }
    },
    "mux": {"enabled": true}
  }
}


```
