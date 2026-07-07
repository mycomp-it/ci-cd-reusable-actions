# ci-cd-reusable-actions

CI riusabile condivisa dell'org `mycomp-it`. Referenziare via `@main`.

## Composite actions (`actions/`)
- `generate-docker-tag` — tag docker dal nome branch (ticket Jira o primi 8 char).
- `create-build-variables` — variabili di build (artifact name, timestamp, SHA, ref).
- `merge-into-integration` — mergia un branch nel branch `integration` e lo pusha; fallisce sui conflitti.

## Reusable workflows (`.github/workflows/`)
- `vue-build-deploy.yml` — build+deploy di una Vue app sullo styles bucket.
- `bo-integration-deploy.yml` — merge→build→deploy dell'ambiente di integrazione bo-pms-webapp (legacy).

## Consumer attuali
- `bo-pms-webapp`, `vue-applications`.
