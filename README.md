## Docker Environment for pantryPlus Ecosystem

Separate docker compose configuration files for each tier in the architecture.

`.env` file is used to collate configurations and `profiles` are used to streamline which bits get started.

## Running

> docker compose --profile mysql up

## Access

You can connect to the MySQL database running within this docker using the following information.

Remember this is just for this local instance; obviously usernames, passwords, and even port numbers should never be shared publicly for sensitive instances.

* Db Port = `3306`
* Host = `localhost`
* User = `root`
* Password = as set in the `MYSQL_ROOT_PASSWORD` environment variable (check `./docker-compose.yaml`)

## Initializing

This is only required the first time you create this resource. Subsequent restarts of this image will retain prior modifications provided you do not delete the docker image.

**Set up the Schema**

* See the `setup.sql` file in the [pantryPlusApiTs Repo](https://github.com/askewsoft/pantryPlusApiTs/tree/main/schema)
