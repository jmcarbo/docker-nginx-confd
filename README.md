```
etcdctl mkdir /webs
etcdctl mkdir /webs/web1
etcdctl set /webs/web1/domain web1.example.com
etcdctl set /webs/web1/subdomain web1
etcdctl set /webs/web1/rootdomain example.com
etcdctl mkdir /webs/web1/upstream

docker run -d -e ETC_ADDR=127.0.0.1:4001 jmcarbo/docker-nginx-confd
```
