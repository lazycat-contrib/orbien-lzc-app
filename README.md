# Orbien for LazyCat

This repository packages [Orbien](https://github.com/orbien-org/orbien) as an LPK v2 application for LazyCat Cloud.

## Runtime configuration

Set `ORBIEN_TOKEN` and `DASHBOARD_PASSWORD` during installation. The dashboard defaults to user `admin`; the generated deployment password is injected into the dashboard login page.

The web dashboard is available through the application entry. TCP and UDP tunnel traffic use port `9527`.

## GitHub Actions

The reusable LazyCat workflow discovers stable `3.x` Orbien server tags, copies the selected GHCR image to LazyCat Registry, builds a versioned LPK Release asset, and publishes to both the official and private stores.

Required GitHub Secrets are `LZC_API_TOKEN`, `APPSTORE_URL`, and `APPSTORE_TOKEN`. Configure `APP_ID` only when the private store application already has a known numeric ID; `PRIVATE_STORE_GROUP_CODES` is needed for private group visibility.

