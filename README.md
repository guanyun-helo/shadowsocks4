# shadowsocks4
* git clone到自己的vps
* 给文件加权限
* 首先执行./ss.sh
* 建议选择ssr
* 然后执行./bbr.sh
* 开启bbr需要kvm内核


Shadowsocks-Python 版：
/etc/init.d/shadowsocks-python start | stop | restart | status

ShadowsocksR 版：
/etc/init.d/shadowsocks-r start | stop | restart | status

Shadowsocks-Go 版：
/etc/init.d/shadowsocks-go start | stop | restart | status

Shadowsocks-libev 版：
/etc/init.d/shadowsocks-libev start | stop | restart | status

### 端口
* firewall-cmd --zone=public --add-port=80/tcp --permanent
* firewall-cmd --zone=public --add-port=80/udp --permanent

### multiport

````
{
    "server":"0.0.0.0",
    "server_ipv6": "[::]",
    "local_address":"127.0.0.1",
    "local_port":1080,
    "port_password":{
        "53":"123456",
        "80":"123456",
        "138":"123456",
        "443":"123456",
        "8080":"123456"
    },
    "timeout":300,
    "method":"chacha20",
    "protocol": "auth_sha1_compatible",
    "protocol_param": "",
    "obfs": "http_simple_compatible",
    "obfs_param": "",
    "redirect": "",
    "dns_ipv6": false,
    "fast_open": false,
    "workers": 1
}
````

