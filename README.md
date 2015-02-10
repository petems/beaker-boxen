# beaker-fog

A Plugin for [Beaker](https://github.com/puppetlabs/beaker), to add an additional hypervisor for Fog servers.

## Supported VPC's

Right now it only works with DigitalOcean, but I can probably fix up the code a little so it's less particular about things.

## Example Nodeset for Beaker

```yaml
HOSTS:
  ubuntu-12.04-amd64-fog-digital-ocean:
    roles:
      - master
    platform: ubuntu-12.04-amd64
    image_id: 9801950 # Ubuntu 12.04.5 x64
    flavor_id: 66 #512MB
    region_id: 7 #London 1
    cloud_provider: DigitalOcean
    hypervisor : fog
    digitalocean_api_key: REDACTED
    digitalocean_client_id: REDACTED
CONFIG:
  type: git
  public_key_path: '/Users/janedoe/.ssh/fog_key.pub'
  private_key_path: '/Users/janedoe/.ssh/fog_key'
```

# Usage

TBC
