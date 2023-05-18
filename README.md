# invoicenija-files
## Invoice Ninja - Docker - Synology Nas

First you need to install `Git Server` for this script to work in your Synology nas! (Go to your package center and search for `Git Server` and install it.

Copy code from script 1
Go to `Control panel` >> `Task Scheduler`
 
#### Script 1
```
mkdir /volume1/docker/ninja-files
sudo git clone https://github.com/wediaz/invoicenija-files.git /volume1/docker/ninja-files
docker run --rm invoiceninja/invoiceninja php artisan key:generate --show > /volume1/docker/ninja-files/key.txt
cd /volume1/docker/ninja-files && rm -r .git && rm *.md
```
