Generate .env file

```sh
export SECRET_ENCRYPTION_KEY=$(openssl rand -hex 32)
envsubst < ./.env.template > ./.env
```
