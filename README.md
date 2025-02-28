# Ref

## Good Links

Good Link : https://medium.chuklee.com/using-skaffold-and-kustomize-for-your-development-a89f2a8b83ed

# Step

## Build
```shell
{
SKAFFOLD_DEFAULT_REPO=k-harbor-01.server.maas/public
skaffold --default-repo="${SKAFFOLD_DEFAULT_REPO}" build
}
```

## Render Manifest ( manifest , kustomize, helm template)
```shell
{
SKAFFOLD_DEFAULT_REPO=k-harbor-01.server.maas/public
skaffold --default-repo="${SKAFFOLD_DEFAULT_REPO}" render
}
```

## Run
```shell
{
SKAFFOLD_DEFAULT_REPO=k-harbor-01.server.maas/public
TARGET_NAMESPACE=gogonggo-dev
skaffold --default-repo="${SKAFFOLD_DEFAULT_REPO}" --namespace=${TARGET_NAMESPACE} run
}
```

# QA
## render
```shell
{
SKAFFOLD_DEFAULT_REPO=k-harbor-01.server.maas/public
TARGET_NAMESPACE=gogonggo-qa
skaffold --default-repo="${SKAFFOLD_DEFAULT_REPO}" --namespace=${TARGET_NAMESPACE} render -p qa
}
```
## Run
```shell
{
SKAFFOLD_DEFAULT_REPO=k-harbor-01.server.maas/public
TARGET_NAMESPACE=gogonggo-qa
skaffold --default-repo="${SKAFFOLD_DEFAULT_REPO}" --namespace=${TARGET_NAMESPACE} run -p qa
}
```

# Google Build


skaffold --default-repo=asia-southeast1-docker.pkg.dev/tidc-poc-gcp2/gogonggo build

gcloud builds submit --config cloudbuild.yaml