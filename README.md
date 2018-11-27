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
docker-compose exec nginx sh -c "apt update && apt install tcpdump && tcpdump udp port 53 -i lo"
```