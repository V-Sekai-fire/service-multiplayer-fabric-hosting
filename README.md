# service-multiplayer-fabric-hosting

A container composition that runs the multiplayer fabric's whole backend on one host, zone server included.

## What it is for

Self-hosting. It runs the accounts and asset API with its web front end, the database and object store behind them, content-addressed chunk serving for zone assets inside the API, a TLS reverse proxy, and one embedded zone server. Further zone servers register with the API on their own.

## Build and run

```sh
git submodule update --init
./generate-secrets.sh
docker compose up -d
```

The API and its web front end build from a `multiplayer-fabric-zone-backend` checkout of `V-Sekai-fire/contract-zone-backend` beside this one, which the submodules do not provide. The secrets script writes `.env`, which holds every setting.

## Licence

MIT. See [LICENSE](LICENSE).
