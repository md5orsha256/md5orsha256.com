## Installing

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
3. Building static files
```sh
docker-compose up --build build
```
---
4. Configure your web server so that it serves static files from the directory specified in the configuration (by default, this is the public directory in the project directory)

OR

You can run
```sh
docker-compose up --build server
```

In order for the hugo server to run. Next, configure your web server so that it redirects requests to localhost port 1313
---


## You are gorgeous!