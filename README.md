# Mark's Docker Compose Files

This repo is meant to be used as a reference for others when creating and managing multiple docker-compose files for use with Traefik as a resverse proxy. I run my containers on an [Alpine Linux](https://alpinelinux.org/) virtual machine.

## Requirements

- [Docker](https://www.docker.com/)
- [docker-compose](https://docs.docker.com/compose/install/)

### Containers

Container | Description | Additional
----------|----------|----------
BitWarden_rs | Password manager | [Hub](https://hub.docker.com/r/bitwardenrs/server)
Matomo | Website Analytics | [Hub](https://hub.docker.com/_/matomo)
Media | Automated media server -  Deluge Jackett Radarr Sonarr | [ReadMe](/media/README.md)
OpenVPN | OpenVPN Server |
Teamspeak | Teamspeak 3 Server | [Hub](https://hub.docker.com/_/teamspeak)
Traefik | Traefik reverse proxy | [Hub](https://hub.docker.com/_/traefik) - [Docs](https://docs.traefik.io/)
Watchtower | Container auto-updates | [Hub](https://hub.docker.com/r/v2tec/watchtower)

#### Environment Files

To keep secrets safe I use .env files in my docker-compose.yml for secrets and passwords. Each should be provided with a .env.example file for example usage

#### Volumes

I create a NFS share on a FreeNAS server for the media containers

#### Installation / Usage

    git clone https://github.com/bearlikelion/docker-compose.git
    cd /<container>/
    docker-compose up -d

## Contributing

Feel free to fork and submit pull requests to this repo
