# cgit

[![coverage report](https://git.shore.co.il/shore/cgit-docker/badges/master/coverage.svg)](https://git.shore.co.il/shore/cgit-docker/-/commits/master)

> cgit Docker image.

## Usage

This container runs Apache that is configured with cgit at `/cgit`. It exposes
port 80 and serves the repositories under `/srv/git`. The container runs as
a limited user (`www-data`), so make sure to have the content of `/srv/git`
readble by it. Also, if you wish to persist the cache, the location is
`/var/cache/cgit`.

## Example usage

```
docker -v '/srv/git:/srv/git:ro' -p '80:80' adarnimrod/cgit
```

There's also a `docker-compose.yml` as further example.

## License

This software is licensed under the MIT license (see `LICENSE.txt`).

## Author Information

Nimrod Adar, [contact me](mailto:nimrod@shore.co.il) or visit my
[website](https://www.shore.co.il/). Patches are welcome via
[`git send-email`](http://git-scm.com/book/en/v2/Git-Commands-Email). The repository
is located at: <https://git.shore.co.il/expore/>.
