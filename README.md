# compose-next-cloud
raspi

version: "2"
services:
  nextcloud:
    image: linuxserver/nextcloud
    container_name: nextcloud
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Europe/Paris
    volumes:
      - /media/nextcloud/config:/config
      - /media/nextcloud/data:/data
    ports:
      - 443:443
    depends_on:
      - mariadb
    restart: unless-stopped
  mariadb:
    image: linuxserver/mariadb
    container_name: mariadb
    environment:
      - PUID=1000
      - PGID=1000
      - MYSQL_ROOT_PASSWORD=123456789
      - TZ=Europe/London
      - MYSQL_DATABASE=nextcloud
      - MYSQL_USER=nextcloud
      - MYSQL_PASSWORD=ABCDEF
    volumes:
      - /media/nextcloud/mariadb:/config
    restart: unless-stopped
