## Deploy

---
1. Clone repository:
```sh
git clone git@github.com:md5orsha256/hugo_personal_site.git
```
---
2. Update submodules (themes)
```sh
git submodule update --init --recursive
```
---
3. setup [certbot](https://certbot.eff.org):

[//]: # (https://pentacent.medium.com/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71)

 - download script
 ```bash
curl -L https://raw.githubusercontent.com/wmnnd/nginx-certbot/master/init-letsencrypt.sh > init-letsencrypt.sh
```

 - Edit the script to add in your domain(s) and your email address. If you’ve changed the directories of the shared Docker volumes, make sure you also adjust the data_path variable as well.

 - make script as executable
```bash
chmod +x init-letsencrypt.sh
```

 - run script:
```bash
sudo ./init-letsencrypt.sh
```

---
4. Run docker
```sh
docker-compose up --build
```
---

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