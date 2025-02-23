# pihole-docker-compose
A docker-compose setup for pi-hole using a local recursive Unbound DNS Resolver.

The included dnsmasq also binds all *.test domains to `127.0.0.1` to make it easy to resolve the same during development.

## Config
First copy the provided `.env.example` to `.env`:
```bash
cp .env.example .env
```

Update the `TIMEZONE` with your desired timezone and `WEBPASSWORD` with a secure😉 one

## Dashboard
The pi-hole dashboard is accessible via port `8053` by default as `http://localhost:8053`, if you wish to use a different port, kindly update [docker-compose.yaml](docker-compose.yaml#L8)

## Running
```bash
docker-compose up -d
```

## Logs
By default, logs are stored in `./data/logs` but you may change this in [docker-compose.yaml](docker-compose.yaml#L17)
