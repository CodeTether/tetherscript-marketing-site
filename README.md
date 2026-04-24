# TetherScript Marketing Site

Static marketing site for TetherScript at `script.codetether.run`.

## Layout

`site/` contains the HTML and CSS served by Nginx.
`nginx/` contains the container server config.
`k8s/` contains the namespaced Kubernetes deployment for `codetether-sites`.

## Deploy

```powershell
gcloud builds submit --project=spotlessbinco --tag us-central1-docker.pkg.dev/spotlessbinco/codetether/tetherscript-marketing-site:v1
kubectl apply -k .
```
