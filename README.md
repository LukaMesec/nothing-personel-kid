#### Clone
````
sudo dd bs=4M if=source of=destion conv=fsync oflag=direct status=progress
````

#### Copy to remote
````
rsync -ah --progress source destination
````

#### List the size (in human readable form) of all sub folders from the current location
````
du -h --max-depth=1
````




