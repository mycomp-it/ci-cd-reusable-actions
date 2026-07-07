# ci-cd-reusable-actions

CI riusabile condivisa dell'org `mycomp-it`. Referenziare via `@main`.

## Composite actions (`actions/`)
- `generate-docker-tag` — tag docker dal nome branch (ticket Jira o primi 8 char).
- `create-build-variables` — variabili di build (artifact name, timestamp, SHA, ref).

## Reusable workflows (`.github/workflows/`)
- `merge-integration.yml` — mergia un branch nel branch `integration` e lo pusha; fallisce sui conflitti. Input `runner` (default `ubuntu-latest`), `secrets.token` per il push. Cross-repo.
- `vue-build-deploy.yml` — build+deploy di una Vue app sullo styles bucket; input `preview_id` per deploy per-PR isolati.

## Consumer attuali
- `bo-pms-webapp`, `vue-applications`.
