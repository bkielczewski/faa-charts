It's a fork of https://github.com/chartbundle/charts with a goal to make it running via Docker.
Initially with minimal changes. Currently tested for sectionals only. 

1. Get Docker
2. Download charts from [FAA](https://www.faa.gov/air_traffic/flight_info/aeronav/digital_products/vfr/), pick Geo-Tiff.
3. Put into ./mapserv/charts
4. Run `docker-compose run makemap /home/mapserv/charts/vfr.sh YYYYMMDD`
5. Run `docker-compose run makemap /home/mapserv/charts/ifr.sh YYYYMMDD` 
6. Run `docker-compose run makemap /home/mapserv/bin/makemap3.pl`, it will take a long while
7. Run `docker-compose up -d`
8. Mapproxy will be available at [http://localhost:8081](http://localhost:8081)
