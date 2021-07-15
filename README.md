# README

* Cloned from operator-sdk folder, to try out Operator build flow

```bash=

export IMG=
export IMAGE_TAG_BASE=

make
make build
make generate
make manifests
make docker-build
make docker-push
make catalog-build
make catalog-push
```
* Requires cert-manager operator

```
make install
make deploy
```
