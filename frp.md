
# Install
`https://github.com/fatedier/frp/releases`


# frps configuration
```ini
[common]
bind_port = 7000
bind_udp_port = 7001
kcp_bind_port = 7000
vhost_http_port = 80
vhost_https_port = 443
dashboard_addr = 0.0.0.0
dashboard_port = 7500
dashboard_user = admin
dashboard_pwd = admin
log_file = ./frps.log
log_level = info
log_max_days = 3
disable_log_color = false
token = 12345678
allow_ports = 2000-3000,3001,3003,4000-50000
max_pool_count = 5
max_ports_per_client = 0
subdomain_host = host
tcp_mux = true
```

# frpc configuration
```ini
[common]
server_addr = ip
server_port = 7000
token = 12345678
log_file = /tmp/frpc.log
log_level = info
log_max_days = 3
tcp_mux = true
protocol = tcp
login_fail_exit = true
user = aaa      

[ae86]
http_user = admin
http_pwd = admin
type = http
local_ip = 172.16.95.13
local_port = 8080
subdomain = ae86
```

# start server & client
`nohup ./frps -c frps.ini >/dev/null 2>&1 &`

# stop
`ps -aux|grep frp| grep -v grep`

`kill -9 pid`
