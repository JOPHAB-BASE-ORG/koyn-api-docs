# Koyn API documentation

Mintlify site for the Koyn REST API. Endpoint pages live under `api-reference/`, concept guides under `guides/`, and site configuration in `docs.json`.

## Local preview

```bash
npm i -g mint
mint dev
```

Open `http://localhost:3000`.

## Checks

```bash
mint validate
mint broken-links
```

## Origin

The endpoint pages were migrated from the team's Postman collection (`GetKoyn.postman_collection.json`, kept in the repo for reference and excluded from the build). Edit the MDX files directly when routes change.

## Publishing

Install the Mintlify GitHub app from the dashboard. Pushes to `main` deploy automatically.
