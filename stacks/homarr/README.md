Generate .env file

```sh
export CLIENT_ID=REPLACE_ME
export CLIENT_SECRET=REPLACE_ME
export SECRET_ENCRYPTION_KEY=$(openssl rand -hex 64)
envsubst < ./.env.template > ./.env
```
