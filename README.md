# octodns docker images

[OctoDNS is DNS as code – a tool for managing DNS across multiple providers](https://github.com/octodns/octodns).

## Usage

```
$ docker run -v "$(pwd):/octodns" --workdir /octodns octodns/octodns octodns-sync
```

This runs `octodns-sync` on the contents of the current working directory.

## Flavors

### 1. 'all'

OctoDNS with all the first-party plugins. [See the list in the requirements.txt for the 'all' flavor.](all/requirements.txt).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/octodns)

### 2. 'cloudflare'

OctoDNS with **only** the [CloudflareProvider](https://github.com/octodns/octodns-cloudflare).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/cloudflare)

## Adding a new flavor

1. Create a new subdirectory, with a `requirements.txt` file.
2. Specify the dependencies you want in `requirements.txt`
3. Add GitHub Actions jobs to both workflows for the new flavor
