# octodns docker images

[OctoDNS is DNS as code – a tool for managing DNS across multiple providers](https://github.com/octodns/octodns).

## Flavors

### 1. 'all'

OctoDNS is pluggable. The `all` flavor includes all first-party plugins.

### 2. 'cloudflare'

OctoDNS with **only** the [CloudflareProvider](https://github.com/octodns/octodns-cloudflare).

## Adding a new flavor

1. Create a new subdirectory, with a Dockerfile and requirements.txt.
2. Specify the dependencies you want in requirements.txt
3. Add GitHub Actions jobs to both workflows for the new flavor
