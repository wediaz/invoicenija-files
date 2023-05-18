# invoicenija-files
Instead of defining our environment variables inside our docker-compose.yml file we now define this in the `env` file, open this file up and insert your `APP_URL`, `APP_KEY` and update the rest of the variables as required.

```
APP_URL=http://in.localhost:8003/
APP_KEY=<insert your generated key in here>
APP_DEBUG=true
REQUIRE_HTTPS=false
IN_USER_EMAIL=
IN_PASSWORD=
```
