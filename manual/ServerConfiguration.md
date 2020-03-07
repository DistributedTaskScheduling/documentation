# Install necessary software
Install docker-ce 1.35+ (Is this the correct version??)
Install postgresql

# Start docker
sudo systemctl start docker

# Database
Make sure to install PostgreSQL.
You may first need to run
```
postgresql-setup --initdb --unit postgresql
```

## Setup postgresql username and password
sudo bash
> su postgres
> > \password postgres

## Change auth mode to username+password
In the pg_hba.conf file (usually in /var/lib/pgsql/data/pg_hba.conf):

```
local   all             all                                     md5
host    all             all             127.0.0.1/32            md5
```

## Restart posgresql
sudo systemctl restart postgresql.service

## Create database
createdb jobadder --owner postgres -U postgres

# Server

Copy the default configuration file to `/etc/jobadder/server.conf`, then adjust the database password (and username, if you do not use the default).
You can also set up an email server connection and web api port.
