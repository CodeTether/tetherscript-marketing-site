# TetherScript Marketing Site

Static marketing site for TetherScript at `script.codetether.run`.

## Layout

`site/` contains the HTML and CSS served by Nginx.
`nginx/` contains the container server config.
`k8s/` contains the namespaced Kubernetes deployment for `codetether-sites`.

## Production Deploy

Production currently runs on Cloud Run using the image in Google Artifact Registry.

```powershell
gcloud builds submit --project=spotlessbinco --tag us-central1-docker.pkg.dev/spotlessbinco/codetether/tetherscript-marketing-site:v1
gcloud run deploy tetherscript-marketing-site --project=spotlessbinco --image=us-central1-docker.pkg.dev/spotlessbinco/codetether/tetherscript-marketing-site:v1 --region=us-central1 --platform=managed --allow-unauthenticated --port=8080
```

## Kubernetes Manifests

The `k8s/` manifests are namespaced under `codetether-sites` for a future cluster deployment.

```powershell
kubectl apply -k .
```
