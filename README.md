# invoicenija-files
## Invoice Ninja - Docker - Synology Nas

First you need to install `Git Server` for this script to work in your Synology nas! (Go to your package center and search for `Git Server` and install it.

Copy code: script 1

Go to `Control panel` >> `Task Scheduler`

Now create a task `Create` >> `Scheduled Task` >> `User-defined script` Task: ninja-files (Or what ever you want) for User: root and click on next tab `Schedule` and choose `Run on the following date` by default I think is "Do not repeat" if not change to `Repeat: Do not repeat` Click on the next tab `Task Settings` and paste the script on `Run command` click ok. Now just select the task and click run, Now open `File Station` and open the ninja-files folder and open the key.txt file and copy the code. Edit the `env` file and paste the code `APP_KEY=` and fill the information and if you need to change ports change them in the `docker-compose.yml` file.


 
#### Script 1
```
mkdir /volume1/docker/ninja-files
sudo git clone https://github.com/wediaz/invoicenija-files.git /volume1/docker/ninja-files
docker run --rm invoiceninja/invoiceninja php artisan key:generate --show > /volume1/docker/ninja-files/key.txt
cd /volume1/docker/ninja-files && rm -r .git && rm *.md
```
Copy code: script 2

next
