# nginx-upstream-server-stress-test
```
root@takaaki-jetson:/etc/nginx/conf.d# pwd
/etc/nginx/conf.d

root@takaaki-jetson:/etc/nginx/conf.d# ll
total 32
drwxr-xr-x 2 root root  4096  ./
drwxr-xr-x 3 root root  4096  ../
-rw-r--r-- 1 root root 13038  400-upstream-servers.conf
-rw-r--r-- 1 root root  4208  default.conf

root@takaaki-jetson:/etc/nginx/conf.d# nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful

root@takaaki-jetson:/etc/nginx/conf.d# nginx -s reload
```
```
root@takaaki-jetson:~# for i in {1..1000}; do date; curl localhost:8888/;sleep 1; echo ""; done
2021å10:12:42 JST
docker 01

2021å10:13:05 JST
docker 01

2021 10:13:06 JST
docker 01

2021 10:13:08 JST
docker 01
```
