```
mkdir C:\git-offline-2204
cd C:\git-offline-2204
```

```
docker run --rm --platform linux/amd64 `
  -v "${PWD}:/out" `
  ubuntu:22.04 bash -c 'set -e; apt-get update; mkdir -p /out/partial; touch /tmp/empty-status; apt-get -y --download-only --no-install-recommends -o Dir::State::status=/tmp/empty-status -o Dir::Cache::archives=/out install git; cd /out; sha256sum *.deb > SHA256SUMS'
```

```
dir C:\git-offline-2204\*.deb
```
