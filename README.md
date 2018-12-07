DNS Resolve
-----------

Run
---

```
docker-compose up --build
```

Debug
-----

```
docker-compose exec nginx sh -c "apt update && apt install -y tcpdump && mv /usr/sbin/tcpdump /usr/bin/tcpdump & tcpdump udp port 53 -i lo"
```

```
03:16:09.146423 IP localhost.53 > localhost.59084: 30770 1/0/0 A 172.18.0.2 (54)
03:16:12.206992 IP localhost.53 > localhost.59084: 53520 1/0/0 A 172.18.0.3 (54)
03:16:21.270984 IP localhost.53 > localhost.59084: 51323 1/0/0 A 172.18.0.2 (54)
03:16:25.356518 IP localhost.53 > localhost.59084: 22385 1/0/0 A 172.18.0.3 (54)
```