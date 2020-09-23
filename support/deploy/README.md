### Install fontello

```sh
# install docker
apt-get update
apt-get install docker.io docker-compose

# create empty directory for docker-compose
git clone https://github.com/fontello/fontello.git

# start server
cd fontello/support/deploy
docker-compose up
```

### Update sources

```sh
cd fontello/support/deploy
docker-compose down
docker-compose build
docker-compose up
```

### Run on localhost

Fontello binds on `https://fontello.com` by default, override it using env variables like this:

```sh
PROTO=http HOST=localhost docker-compose up
```
