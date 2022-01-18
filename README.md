# octodns docker images

[OctoDNS is DNS as code – a tool for managing DNS across multiple providers](https://github.com/octodns/octodns).

## Usage

```
$ docker run -v "$(pwd):/octodns" --workdir /octodns octodns/<flavor> octodns-sync

# Example:
$ docker run -v "$(pwd):/octodns" --workdir /octodns octodns/octodns octodns-sync
```

This runs `octodns-sync` on the contents of the current working directory.

## Flavors

| Flavor | Module | Docker Hub |
|--------|--------|------------|
| azure | [octodns_azure](https://github.com/octodns/octodns-azure) | [octodns/azure](https://hub.docker.com/r/octodns/azure) |
| cloudflare | [octodns_cloudflare](https://github.com/octodns/octodns-cloudflare) | [octodns/cloudflare](https://hub.docker.com/r/octodns/cloudflare) |
| constellix | [octodns_constellix](https://github.com/octodns/octodns-constellix) | [octodns/constellix](https://hub.docker.com/r/octodns/constellix) |
| digitalocean | [octodns_digitalocean](https://github.com/octodns/octodns-digitalocean) | [octodns/digitalocean](https://hub.docker.com/r/octodns/digitalocean) |
| dnsimple | [octodns_dnsimple](https://github.com/octodns/octodns-dnsimple) | [octodns/dnsimple](https://hub.docker.com/r/octodns/dnsimple) |
| dnsmadeeasy | [octodns_dnsmadeeasy](https://github.com/octodns/octodns-dnsmadeeasy) | [octodns/dnsmadeeasy](https://hub.docker.com/r/octodns/dnsmadeeasy) |
| dyn | [octodns_dyn](https://github.com/octodns/octodns-dyn) | [octodns/dyn](https://hub.docker.com/r/octodns/dyn) |
| easydns | [octodns_easydns](https://github.com/octodns/octodns-easydns) | [octodns/easydns](https://hub.docker.com/r/octodns/easydns) |
| edgedns | [octodns_edgedns](https://github.com/octodns/octodns-edgedns) | [octodns/edgedns](https://hub.docker.com/r/octodns/edgedns) |
| etchosts | [octodns_etchosts](https://github.com/octodns/octodns-etchosts) | [octodns/etchosts](https://hub.docker.com/r/octodns/etchosts) |
| gandi | [octodns_gandi](https://github.com/octodns/octodns-gandi) | [octodns/gandi](https://hub.docker.com/r/octodns/gandi) |
| gcore | [octodns_gcore](https://github.com/octodns/octodns-gcore) | [octodns/gcore](https://hub.docker.com/r/octodns/gcore) |
| googlecloud | [octodns_googlecloud](https://github.com/octodns/octodns-googlecloud) | [octodns/googlecloud](https://hub.docker.com/r/octodns/googlecloud) |
| hetzner | [octodns_hetzner](https://github.com/octodns/octodns-hetzner) | [octodns/hetzner](https://hub.docker.com/r/octodns/hetzner) |
| mythicbeasts | [octodns_mythicbeasts](https://github.com/octodns/octodns-mythicbeasts) | [octodns/mythicbeasts](https://hub.docker.com/r/octodns/mythicbeasts) |
| ns1 | [octodns_ns1](https://github.com/octodns/octodns-ns1) | [octodns/ns1](https://hub.docker.com/r/octodns/ns1) |
| ovh | [octodns_ovh](https://github.com/octodns/octodns-ovh) | [octodns/ovh](https://hub.docker.com/r/octodns/ovh) |
| powerdns | [octodns_powerdns](https://github.com/octodns/octodns-powerdns) | [octodns/powerdns](https://hub.docker.com/r/octodns/powerdns) |
| rackspace | [octodns_rackspace](https://github.com/octodns/octodns-rackspace) | [octodns/rackspace](https://hub.docker.com/r/octodns/rackspace) |
| route53 | [octodns_route53](https://github.com/octodns/octodns-route53) | [octodns/route53](https://hub.docker.com/r/octodns/route53) |
| selectel | [octodns_selectel](https://github.com/octodns/octodns-selectel) | [octodns/selectel](https://hub.docker.com/r/octodns/selectel) |

## Adding a new flavor

1. Add the module to the `all/requirements.txt` file
2. Run `script/generate-workflow-file` (requires PyYaml module)
3. Copy-and-paste the markdown table from the output into `README.md`

## Updating a version

Update the version in `all/requirements.txt` – it will be used in the 'all' flavor and the provider-specific flavor.
