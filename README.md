# TetherScript Marketing Site

Static marketing site for TetherScript at `script.codetether.run`.

## Layout

`site/` contains the HTML and CSS served by Nginx.
`nginx/` contains the container server config.
`k8s/` contains the namespaced Kubernetes deployment for `codetether-sites`.

## Deploy

```powershell
kubectl apply -k .
```
