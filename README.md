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

# Testing the Catalog/Bundle

```bash=

make bundle bundle-build bundle-push

(base) ➜  memcached-operator git:(make-clean) ✗ operator-sdk run bundle quay.io/cdoan/memcached-operator-bundle:v0.0.1
I0720 13:15:54.389549   25908 request.go:655] Throttling request took 1.193332997s, request: GET:https://api.dell-r730-008.demo.red-chesterfield.com:6443/apis/samples.operator.openshift.io/v1?timeout=32s
INFO[0016] Successfully created registry pod: quay-io-cdoan-memcached-operator-bundle-v0-0-1
INFO[0016] Created CatalogSource: memcached-operator-catalog
INFO[0016] Created Subscription: memcached-operator-v0-0-1-sub
INFO[0019] Approved InstallPlan install-dlrw8 for the Subscription: memcached-operator-v0-0-1-sub
INFO[0019] Waiting for ClusterServiceVersion "memcached-operator-system/memcached-operator.v0.0.1" to reach 'Succeeded' phase
INFO[0019]   Waiting for ClusterServiceVersion "memcached-operator-system/memcached-operator.v0.0.1" to appear
INFO[0026]   Found ClusterServiceVersion "memcached-operator-system/memcached-operator.v0.0.1" phase: Pending
INFO[0029]   Found ClusterServiceVersion "memcached-operator-system/memcached-operator.v0.0.1" phase: Installing
INFO[0039]   Found ClusterServiceVersion "memcached-operator-system/memcached-operator.v0.0.1" phase: Succeeded
INFO[0039] OLM has successfully installed "memcached-operator.v0.0.1"
```
