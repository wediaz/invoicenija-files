# invoicenija-files
## Invoice Ninja - Docker - Synology Nas

First you need to install `Git Server` for this script to work in your Synology nas! (Go to your package center and search for `Git Server` and install it.

Copy code: script 1

Go to `Control panel` >> `Task Scheduler`

Now create a task `Create` >> `Scheduled Task` >> `User-defined script` Task: ninja-files (Or what ever you want) for User: root and click on next tab `Schedule` and choose `Run on the following date` 


 
#### Script 1
```
mkdir /volume1/docker/ninja-files
sudo git clone https://github.com/wediaz/invoicenija-files.git /volume1/docker/ninja-files
docker run --rm invoiceninja/invoiceninja php artisan key:generate --show > /volume1/docker/ninja-files/key.txt
cd /volume1/docker/ninja-files && rm -r .git && rm *.md
```
