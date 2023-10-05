# GRUSP DOCKER

Deploy of GRUSP site with Docker.

## Configuration

The default values are meant for local development.

| env                | default        | description                        |
| ------------------ | -------------- | ---------------------------------- |
| `DOMAIN`           | `grusp.test`   | The domain for the application     |
| `DB_DATABASE`      | `laravel`      | Database name                      |
| `DB_USERNAME`      | `laravel`      | Database username                  |
| `DB_PASSWORD`      | `password`     | Database password                  |
| `DB_PASSWORD_ROOT` | `passwordroot` | Database root password             |
| `DIR_API`          | `../grusp-api` | Directory path to GRUSP API        |
| `DIR_ADM`          | `../grusp-adm` | Directory path to GRUSP ADM        |
| `DIR_APP`          | `../grusp-app` | Directory path to GRUSP APP        |
| `CMD_ADM`          | `npm run dev`  | Command to be run by adm container |
| `CMD_APP`          | `npm run dev`  | Command to be run by app container |

### `DOMAIN`

GRUSP APP wil be available at domain `${DOMAIN}`.
GRUSP ADM wil be available at subdomain `adm.${DOMAIN}`.
GRUSP API wil be available at subdomain `api.${DOMAIN}`.

### CMD ADM

In development mode, it should be `npm run dev`.

In produnction mode, it should be `sh -c "npm run build && npm run start"`.

### CMD APP

In development mode, it should be `npm run dev`.

In produnction mode, it should be `sh -c "npm run build && npm run start"`.
