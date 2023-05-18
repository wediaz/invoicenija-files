# invoicenija-files
## Invoice Ninja - Docker Install - Synology Nas

First you need to install `Git Server` for this script to work! (Go to your package center and search for `Git Server` and install it.
 variables inside our docker-compose.yml file we now define this in the `env` file, open this file up and insert your `APP_URL`, `APP_KEY` and update the rest of the variables as required.

```
mkdir /volume1/docker/ninja-files
sudo git clone https://github.com/wediaz/invoicenija-files.git /volume1/docker/ninja-files
docker run --rm invoiceninja/invoiceninja php artisan key:generate --show > /volume1/docker/ninja-files/key.txt
cd /volume1/docker/ninja-files && rm -r .git && rm *.md
```
