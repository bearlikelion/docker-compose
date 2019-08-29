# Mark's Docker Compose Files

This repo is meant to be informational and used as a reference for others when creating and managing multiple docker-compose files with Traefik acting as a reverse proxy.

I run my containers on an [Alpine Linux](https://alpinelinux.org/) virtual machine.

## Requirements

- [Docker](https://www.docker.com/)
- [docker-compose](https://docs.docker.com/compose/install/)

### Containers

Container | Description | Additional
----------|----------|----------
BitWarden_rs | Password manager | [Hub](https://hub.docker.com/r/bitwardenrs/server)
Matomo | Website Analytics | [Hub](https://hub.docker.com/_/matomo)
Media | Automated media server -  Deluge Jackett Radarr Sonarr | [ReadMe](/media/README.md)
Netdata | Performance monitoring | [Hub](https://hub.docker.com/r/netdata/netdata/)
Nextcloud | A safe home for all your data | [Hub](https://hub.docker.com/_/nextcloud)
OpenVPN | OpenVPN Server | **Work in progress**
Organizr | HTPC/Homelab services organizer | [Hub](https://hub.docker.com/r/organizrtools/organizr-v2)
Pi-hole | Network based ad blocker | [Hub](https://hub.docker.com/r/pihole/pihole) - [Website](https://pi-hole.net/)
Relay | Tor Relay Server | [Hub](https://hub.docker.com/r/brunneis/tor-relay-arm)
Teamspeak | Teamspeak 3 Server | [Hub](https://hub.docker.com/_/teamspeak)
Traefik | Traefik reverse proxy | [Hub](https://hub.docker.com/_/traefik) - [Docs](https://docs.traefik.io/)
Warrior | Archive Team warrior | [Hub](https://hub.docker.com/r/archiveteam/warrior-dockerfile/)
Watchtower | Container auto-updates | [Hub](https://hub.docker.com/r/v2tec/watchtower)

#### Environment Files

To keep secrets safe I use .env files in my docker-compose.yml for secrets and passwords.\
Each should be provided with a .env.example file for example usage

#### Volumes

I mount NFS Shared from my FreeNAS Server for external storage to the containers (media, nextcloud, warrior)

#### Installation / Usage

    git clone https://github.com/bearlikelion/docker-compose.git
    cd /<container>/
    docker-compose up -d

##### Contributing

Feel free to fork and submit pull requests to this repo
