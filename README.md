# service-multiplayer-fabric-hosting

A container composition that runs the multiplayer fabric's whole backend on one host, zone server included.

## What it is for

Self-hosting. It runs the accounts and asset API with its web front end, the database and object store behind them, a content-addressed chunk server for zone assets, a TLS reverse proxy, and one embedded zone server. Further zone servers register with the API on their own.

## Build and run

```sh
git submodule update --init
./generate-secrets.sh
docker compose up -d
```

The secrets script writes `.env`, which holds every setting.

## Licence

The licence is not stated.
