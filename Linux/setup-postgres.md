# Setup PostgresSQL in Ubuntu/Debian
## Update Repo
```bash
sudo apt update
sudo apt upgrade
```

## Install PostgressSQL
```sh
sudo apt install postgresql postgresql-contrib
```

##  Verify PostgreSQL Installation
```sh
sudo systemctl status postgresql
```
## Configure
By default postgres creates a user called `postgres` in the system we need to switch to that user by following
```sh
sudo -i -u postgres
```
### Create a new user
Run `createuser --interactive` which will ask you the following

```
Enter name of role to add: username
Shall the new role be a superuser? (y/n) y
```

