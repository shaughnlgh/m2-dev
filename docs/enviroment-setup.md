# Environment Setup

For this section, we will use the Warden CLI uility for orchestrating the Docker based developer environment. I will 
guide you through the setup Warden process, but feel free to read over the [Warden docs](https://docs.warden.dev/index.html)
if you want more info or just to familiarise yourself with the utility.

Warden is used because it supports multiple frameworks like M1, M2, Laravel, etc. It also helps maintain the same tech 
stack within your development team and closely mimics every service that would be used in a production environment.

- [System requirements and setups](#system-requirements-and-setups)

- [Prerequisites](#prerequisites)

- [Magento environment setup](#magento-environment-setup)

## System requirements and setups

| Package/Apps   | Version  |
|----------------|----------|
| Docker Desktop | 2.2.0.0+ |
| docker-compose | 1.25.0+  |
| Homebrew       | 3.4.0+   |

### Docker Desktop

1. Download and install from <https://www.docker.com/products/docker-desktop/>

2. Once installed, assign at least 6GB RAM (8GB recommended) to Docker Desktop in `Preferences -> Resources -> Advanced -> Memory`.

### Homebrew

Install and follow command prompts:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

For additional info see <https://brew.sh/>
   
### docker-compose

Install and follow command prompts:
```bash
brew install docker-compose
```

### Warden

Install and follow command prompts:
```bash
brew install davidalger/warden/warden
warden svc up
```

You should now have a new container called `warden` with several global services running in that container. 
To confirm, run:
```bash
docker ps
```
Output
![docker ps output](images/docker-ps-output-1.png)

The following URL's can be used to interact with the UI's for services Warden runs globally:

- Traefik - <https://traefik.warden.test/> - Reverse proxy and load balancer.
- Portainer - <https://portainer.warden.test/> - Docker container management.
- Dnsmasq - <https://dnsmasq.warden.test/> - DNS management.
- MailHog - <https://mailhog.warden.test/> - Fake SMTP mail server for email testing. 


## Prerequisites

1. Create a personal access token (with read/write permissions) on GitLab, Github or BitBucket.

2. Create your access tokens on the Magento marketplace.


## Magento environment setup

