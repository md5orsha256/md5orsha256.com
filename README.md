## Deploy

Deployment happens automatically in [gh-actions](https://github.com/features/actions) on [gh-pages](https://pages.github.com). See the [gh-pages.yaml](.github/workflows/gh-pages.yaml) file for the delivery configuration.

## Development
Before pulling git repo run docker image for serving development server:

```bash
docker run --rm -it \
  -v $(pwd):/src \
  -p 1313:1313 \
  klakegg/hugo:0.80.0 \
  server 
```

---


You are gorgeous!