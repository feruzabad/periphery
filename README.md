# periphery

Komodo Periphery (remote agent), run with Docker Compose. Periphery is what Komodo uses to manage a host, so it is deployed from this repo and not by Komodo.

## Install

    sudo install -d -o "$USER" -g "$USER" /opt/periphery
    git clone git@github.com:feruzabad/periphery.git /opt/periphery
    cd /opt/periphery
    cp env.example .env && chmod 600 .env && $EDITOR .env
    docker compose up -d

`.env` and `keys/` are git-ignored. Remove `PERIPHERY_ONBOARDING_KEY` from `.env` once the server shows up in Komodo.

## Update

    cd /opt/periphery && git pull && docker compose up -d

Renovate bumps the image tag (and digest) in `compose.yaml`.
