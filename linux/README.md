#### Clone 
````
sudo dd bs=4M if=source of=destion conv=fsync oflag=direct status=progress
````

#### Copy to remote
````
rsync -ah --progress source destination
````

#### download: remote -> local (with key)
````
 sudo scp -r -i /home/lukaa/.ssh/key user@host:path local_path
````

#### download: remote -> local
````
scp user@remote_host:remote_file local_file 
````

#### upload: local -> remote
````
scp local_file user@remote_host:remote_file
````

#### List the size (in human readable form) of all sub folders from the current location
````
du -h --max-depth=1

````
#### Exec time limit mysql (importing large .sql dumps)
````
./usr/share/phpmyadmin/libraries/config.default.php
````

#### PLEX stuff

````
sudo systemctl enable plexmediaserver.service
sudo systemctl start plexmediaserver.service
sudo systemctl status plexmediaserver.service
sudo systemctl stop plexmediaserver.service

````


#### MYSQL stuff

````
USE ime_baze;
````

````
select email from info where type like "%informacijsko%" or type like "%računal%" or type like "%progr%" INTO OUTFILE "/tmp/rezultat.txt";

````

#### Pihole stuff

Get password
````
docker logs pihole | grep random

````

````
docker run -d \
    --name pihole \
    -p 53:53/tcp -p 53:53/udp \
    -p 80:80 \
    -e TZ="America/Chicago" \
    -v "${PIHOLE_BASE}/etc-pihole:/etc/pihole" \
    -v "${PIHOLE_BASE}/etc-dnsmasq.d:/etc/dnsmasq.d" \
    --dns=127.0.0.1 --dns=1.1.1.1 \
    --restart=unless-stopped \
    --hostname pi.hole \
    -e VIRTUAL_HOST="pi.hole" \
    -e PROXY_LOCATION="pi.hole" \
    -e ServerIP="127.0.0.1" \
    pihole/pihole:latest
````

Run nextcloud with volume on 8085
````
docker run -d -p 8085:80\
	-v nextcloud:/var/www/html \
	-v apps:/var/www/html/custom_apps \
	-v config:/var/www/html/config \
	-v data:/var/www/html/data \
	nextcloud
````


Run apache with php
````
docker run -d -p 8085:80 --name my-apache-php-app -v "$PWD":/var/www/html php:7.4-apache
````
enable pdo-mysql, exec in container

````
docker-php-ext-install pdo pdo_mysql
````
