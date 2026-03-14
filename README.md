# Nginx_1.28.2
Nginx_1.28.2　Windows版

Ngnix官网的发行版以网段为单位进行数据分发和均衡流量，同局域网内负载均衡便会失效。
现修改为以IP地址为单位，同局域网内有效。
仅提供32Bit编译版。64Bit版编译有丢失精度可能，需要的请自行编译。

The official releases of Nginx distribute and balance traffic by subnet, which renders load balancing ineffective within the same LAN.
We've now modified it to distribute traffic by IP address, which is effective within the same LAN. Only the 32-bit compilation version is provided. Please note that compiling a 64-bit version may result in precision loss, so if needed, please compile it yourself.

-------------------------------------------------------------------------------------------------
To Build：
```
./auto/configure	\
	--with-cc=cl	\
	--builddir=objs	\
	--with-debug	\
	--prefix= 	\
	--conf-path=conf/nginx.conf		\
	--pid-path=logs/nginx.pid	\
	--http-log-path=logs/access.log		\
	--error-log-path=logs/error.log		\
	--sbin-path=nginx.exe		\
	--http-client-body-temp-path=temp/client_body_temp	\
	--http-proxy-temp-path=temp/proxy_temp		\
	--http-fastcgi-temp-path=temp/fastcgi_temp		\
	--http-scgi-temp-path=temp/scgi_temp	\
	--http-uwsgi-temp-path=temp/uwsgi_temp	\
	--with-cc-opt=-DFD_SETSIZE=1024		\
	--with-pcre=objs/lib/pcre2-10.46	\
	--with-zlib=objs/lib/zlib-1.3.1		\
	--with-http_v2_module				\
	--with-http_realip_module			\
	--with-http_addition_module			\
	--with-http_sub_module				\
	--with-http_dav_module				\
	--with-http_stub_status_module		\
	--with-http_flv_module				\
	--with-http_mp4_module				\
	--with-http_gunzip_module			\
	--with-http_gzip_static_module		\
	--with-http_auth_request_module		\
	--with-http_random_index_module		\
	--with-http_secure_link_module		\
	--with-http_slice_module			\
	--with-mail		\
	--with-stream	\
	--with-stream_realip_module			\
	--with-stream_ssl_preread_module	\
	--with-openssl=objs/lib/openssl-3.5.4	\
	--with-openssl-opt="no-asm no-tests no-makedepend	\
		-D_WIN32_WINNT=0x0501"		\
	--with-http_ssl_module			\
	--with-mail_ssl_module			\
	--with-stream_ssl_module

  nmake

```
