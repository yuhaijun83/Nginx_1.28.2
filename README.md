# Nginx_1.28.2
Nginx_1.28.2　Windows版

Ngnix官网的发行版以网段为单位进行数据分发和均衡流量，同局域网内负载均衡便会失效。
现修改为以IP地址为单位，同局域网内有效。
仅提供32Bit编译版。64Bit版编译有丢失精度可能，需要的请自行编译。

The official releases of Nginx distribute and balance traffic by subnet, which renders load balancing ineffective within the same LAN.
We've now modified it to distribute traffic by IP address, which is effective within the same LAN. Only the 32-bit compilation version is provided. Please note that compiling a 64-bit version may result in precision loss, so if needed, please compile it yourself.

