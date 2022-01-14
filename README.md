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

### 1. 'all'

OctoDNS with all the first-party plugins. [See the list in the requirements.txt for the 'all' flavor.](all/requirements.txt).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/octodns)

### 2. 'azure'

OctoDNS with **only** the [AzureProvider](https://github.com/octodns/octodns-azure).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/azure)

### 3. 'cloudflare'

OctoDNS with **only** the [CloudflareProvider](https://github.com/octodns/octodns-cloudflare).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/cloudflare)

### 4. 'constellix'

OctoDNS with **only** the [ConstellixProvider](https://github.com/octodns/octodns-constellix).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/constellix)

### 5. 'digitalocean'

OctoDNS with **only** the [DigitalOceanProvider](https://github.com/octodns/octodns-digitalocean).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/digitalocean)

### 6. 'dnsimple'

OctoDNS with **only** the [DNSimpleProvider](https://github.com/octodns/octodns-dnsimple).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/dnsimple)

### 7. 'dnsmadeeasy'

OctoDNS with **only** the [DNSMadeEasyProvider](https://github.com/octodns/octodns-dnsmadeeasy).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/dnsmadeeasy)

### 8. 'dyn'

OctoDNS with **only** the [DynProvider](https://github.com/octodns/octodns-dyn).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/dyn)

### 9. 'edgedns'

OctoDNS with **only** the [AkamaiProvider](https://github.com/octodns/octodns-edgedns).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/edgedns)

### 10. 'etchosts'

OctoDNS with **only** the [EtcHostsProvider](https://github.com/octodns/octodns-etchosts).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/etchosts)

### 11. 'gandi'

OctoDNS with **only** the [GandiProvider](https://github.com/octodns/octodns-gandi).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/gandi)

### 12. 'ns1'

OctoDNS with **only** the [Ns1Provider](https://github.com/octodns/octodns-ns1).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/ns1)

### 13. 'powerdns'

OctoDNS with **only** the [PowerDNSProvider](https://github.com/octodns/octodns-powerdns).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/powerdns)

### 14. 'route53'

OctoDNS with **only** the [Route53Provider](https://github.com/octodns/octodns-route53).

[View on Docker Hub &rarr;](https://hub.docker.com/r/octodns/route53)

## Adding a new flavor

1. Create a new subdirectory, with a `requirements.txt` file.
2. Specify the dependencies you want in `requirements.txt`
3. Add GitHub Actions jobs to both workflows for the new flavor

## Updating a version

Update the version in `all/requirements.txt` – it will be used in the 'all' flavor and the provider-specific flavor.
