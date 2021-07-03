# fairplay_server Deployconf

Quick and dirty deployment configuration.

## How to use

1. Clone `fairplay_server` project in this projects directory.
2. Clone `FairplayKSM` into `fairplay_server/docker` as mentioned in the readme of `fairplay_server`.
3. Run the following command to get a Djano secret key:
   ```shell
   docker run --rm django python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
   ```
4. Copy `.env.example`to `.env` and fill out all empty settings.
5. Put the private key at `secrets/dev_private_key.pem`
6. Put the ASK at `secrets/ask`
7. `docker-compose up -d`