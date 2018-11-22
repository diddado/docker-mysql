Mysql

You need a ```.env``` file to set the required parameters.  It should look like this:

```bash
COMPOSE_PROJECT_NAME=mysql # this should be unique for every version of mysql since the data volume will be persisted and will be named based on this value.
MYSQL_VERSION=5.7 # the container version you want to use
MYSQL_ROOT_PASSWORD=YourRootPasswordHere
MYSQL_USER=YourRegularUserNameHere
MYSQL_PASS=YourRegularUserPasswordHere
MYSQL_DATABASE=YourDatabaseNameHere
```

Run ```docker-compose up``` to start the container.

The configuraation will default to version 5.7 if a .env file isn't created. 

You will run into data conflicts if you run multiple versions and don't set COMPOSE_PROJECT_NAME in the .env file.

The best way to access the server is with Sequel Pro
https://sequelpro.com/
