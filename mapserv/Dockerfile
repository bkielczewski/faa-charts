FROM debian:bullseye-slim

COPY bin/ /home/mapserv/bin/
COPY basemap/ /home/mapserv/basemap/
COPY grid/ /home/mapserv/grid/
COPY mapfiles/ /home/mapserv/mapfiles/
COPY perl/ /home/mapserv/perl/

RUN apt update \
    && apt install -y --no-install-recommends \
    proj-bin  \
    proj-data  \
    libgdal-perl  \
    python3-gdal  \
    gdal-bin mapserver-bin  \
    && rm -rf /var/lib/apt/lists  \
    && rm -rf /var/cache/apt

VOLUME /home/mapserv/charts
WORKDIR /home/mapserv
