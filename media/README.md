# Mark's Media Server

Mark's docker-compose file for his automated media server. Containers provided by [linuxserver.io](https://linuxserver.io)

## Containers

Container | Description | Additional
----------|----------|----------
Deluge | Torrent Client | [Hub](https://hub.docker.com/r/linuxserver/deluge)
Jackett | Torrent Indexer | [Hub](https://hub.docker.com/r/linuxserver/jackett)
Radarr  | Movie Downloader | [Hub](https://hub.docker.com/r/linuxserver/radarr)
Sonarr | Television Downloader | [Hub](https://hub.docker.com/r/linuxserver/sonarr)
Tautulli | Plex Analytics and Statistics | [Hub](https://hub.docker.com/r/linuxserver/tautulli)

### Volumes

I mount a NFS Media Share to the containers in the docker-compose file
