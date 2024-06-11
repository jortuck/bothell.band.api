### Deployment

This instance is configured with Docker & Docker Compose.
You will need to create a copy of `.env.example` and rename it to `.env`.
Be sure to set the roper environment variables.

The production and development configurations share the same Postgres database.

**This specific instance runs on port `1338`**.

#### Run the development instance:
```
docker compose --profile dev up -d --build
```
#### Run the production instance
```
docker compose --profile prod up -d --build
```
#### Don't forget to use the respective down command.
```
docker compose --profile dev down -d --build
```
or
```
docker compose --profile prod down -d --build
```
#### Running Commands Inside The Container
```
docker compose exec jordan-api 
```
```
docker compose exec jordan-api-prod
```
#### Data Transfer
```
docker compose exec jordan-api yarn strapi transfer --{from/to} {url}
```

# 🚀 Getting started with Strapi

Strapi comes with a full featured [Command Line Interface](https://docs.strapi.io/dev-docs/cli) (CLI) which lets you scaffold and manage your project in seconds.

### `develop`

Start your Strapi application with autoReload enabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-develop)

```
npm run develop
# or
yarn develop
```

### `start`

Start your Strapi application with autoReload disabled. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-start)

```
npm run start
# or
yarn start
```

### `build`

Build your admin panel. [Learn more](https://docs.strapi.io/dev-docs/cli#strapi-build)

```
npm run build
# or
yarn build
```

