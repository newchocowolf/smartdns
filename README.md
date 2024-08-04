# Smart DNS

Stupidly simple Smart DNS proxy to watch Netflix.

## you can build this with 
```bash
docker build -t dns-proxy .
```

## you can run the script with this code
```bash
docker run -d --cap-add=NET_ADMIN -p 53:53/udp -p 443:443 -p 80:80 -e IP=your-ip-address --log-opt max-size=10m --log-opt max-file=3 dns-proxy
```

## Variables
| ENV  |  Default  |  Description  |
|---|---|---|
| IP  | 127.0.0.1  | Your public ip for server  |
| ALLOWED_IP | 0.0.0.0/0  | Your allowed ip for client |
