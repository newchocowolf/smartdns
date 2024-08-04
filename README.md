# Smart DNS

Stupidly simple Smart DNS proxy to watch Netflix.

## you can build this with 
```bash
docker build -t dns-proxy .
```

## you can run the script with this code
```bash
docker run -d --name dns-proxy-container -e IP=<your_public_ip> -p 53:53/udp -p 80:80 -p 443:443 dns-proxy
```

## Variables
| ENV  |  Default  |  Description  |
|---|---|---|
| IP  | 127.0.0.1  | Your public ip for server  |
| ALLOWED_IP | 0.0.0.0/0  | Your allowed ip for client |
