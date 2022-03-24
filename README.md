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


