# nsswitch_dns

Based on: jpillora/dnsmasq && [90dns](https://gitlab.com/a/90dns)

## Run the container
```
$ docker run \
    --name dnsmasq \
    -d \
    -p 53:53/udp \
    -p 5380:8080 \
    --log-opt "max-size=100m" \
    -e "HTTP_USER=root" \
    -e "HTTP_PASS=root" \
    --restart always \
    jpillora/dnsmasq
```