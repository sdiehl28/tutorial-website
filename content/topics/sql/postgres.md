---
title: PostgreSQL
weight: 30
lastmod: 2019-01-19

# typora requires yaml, not toml
typora-root-url: /home/agni/WebSites/published/tutorial-website/static/
---

PostgreSQL is also called Postgres.

An excellent book is: [PostgreSQL Up & Running 3rd Edition](https://www.amazon.com/PostgreSQL-Running-Practical-Advanced-Database/dp/1491963417/)

An excellent book on SQL, specifically Postgres SQL is: [Practical SQL](https://www.amazon.com/Practical-SQL-Beginners-Guide-Storytelling-ebook/dp/B07197G78H/) 

The following instructions are for beginners.  They are verbose.  If you are an expert, you may chose to do something different.

The following instructions will:

1. Install postgres on Ubuntu
2. Change the default authentication method for the postgres user
3. Change the default password for the postgres user
4. Install pgAdmin4 in a Python virtual environment
5. Configure pgAdmin4 to use desktop mode
6. Add your existing postgres server to pgAdmin4
7. Create an example database
8. Install iPython sql magic extension

### Postgres Installation for Ubuntu

#### Choose Version

You can install Postgres using apt.  To see what version apt will provide, enter the following at the terminal: 
```bash
apt-cache policy postgresql
```

You may find that this version is too old for you. 

You can install Postgres using snap.  To see what versions snap offers, enter the following at the terminal:
```bash
# try version 10
snap find postgresql10

# try version 11
snap find postgresql11
```
You may find that these versions are also too old for you.

The following are the instructions for getting the latest version of postgres for your version of Ubuntu from the Postgres website.

### Install from Postgres website

```bash
# add security key
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

# add repo for your version of ubuntu
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ $(lsb_release -sc)-pgdg main" > /etc/apt/sources.list.d/PostgreSQL.list'

# update
sudo apt update

# install version 10
#apt install postgresql-10

# install version 11
apt install postgresql-11

# it is no longer necessary to separately download postgresql client apps
```
The install should setup the postgres service so that is starts automatically on reboot and start it (so you don't have to reboot).

```bash
# helpful command for working with the postgres server
# enable the service to start at boot
sudo systemctl enable postgresql.service

# stop the service
sudo systemctl stop postgresql.service

# check on the status of the service
sudo systemctl status postgresql.service

# start the service
sudo systemctl start postgresql.service

# restart the service
sudo systemctl restart postgresql.service
```

### Verify installation

```bash
# switch to user postgres in a login shell
sudo su -l postgres

# run psql command line utility
psql
postgres=#  \conninfo

# \conninfo show return something like:
# You are connected to database "postgres" as user "postgres" via socket in "/var/run/postgresql" at port "5432".

# change the postgres user password (for later authentication with md5)
postgres=# \password
# enter your password
```

### Install pgadmin4

Download the wheel from: [pgAdmin4 Python Wheel](https://www.pgadmin.org/download/pgadmin-4-python-wheel/)

Chose one of the latest versions to download.

Create a Python Virtual Environment:

```bash
# chose a directory where you want it installed
# for example
cd ~/bin
python3 -m venv pgadmin4

# activate the virtual environment
source pgadmin4/bin/activate

# install the pgAdmin4 wheel
# for example
pip install ~/Downloads/pgadmin4-4.1-py2.py3-none-any.whl
```

The default Postgres authentication is peer.  This means the Linux user must match the Postgres user.  I find this inconvenient, especially as I just created a venv under my usual Linux login user.

At installation, the postgres user: postgres was created.  I like to run pgadmin4 as user: postgres

Change the postgres server authentication method for user postgres:

```bash
# find the configuration file
sudo su -l postgres

# run psql command line utility
psql
postgres=# SHOW hba_file;
postgres=# exit

# edit the configuration file
# for example
sudo su -c "vi /etc/postgresql/11/main/pg_hba.conf" postgres
# find the entry for postgres and change peer to md5, exit your editor

# restart the server
sudo systemctl restart postgresql.service
```

Create a pgAdmin4 configuration file.  This matters because the default is to run pgAdming4 in server mode whereas we are running the postgres server locally and we want to run pgAdmin4 locally as well.

```bash
# create file: pgadmin4/lib/python3.7/site-packages/pgadmin4/config_local.py
# with the following contents
import os
DATA_DIR = os.path.realpath(os.path.expanduser(u'~/.pgadmin/'))
LOG_FILE = os.path.join(DATA_DIR, 'pgadmin4.log')
SQLITE_PATH = os.path.join(DATA_DIR, 'pgadmin4.db')
SESSION_DB_PATH = os.path.join(DATA_DIR, 'sessions')
STORAGE_DIR = os.path.join(DATA_DIR, 'storage')
SERVER_MODE = False
```

Make it easier to start pgAdmin4:

```bash
vi pgadmin4/lib/python3.7/site-packages/pgadmin4/pgAdmin4.py
# add as the very first line, where <you> is the result of: whoami
#!/home/<you>/bin/pgadmin4/bin/python

# make it executable
chmod 755 pgadmin4/lib/python3.7/site-packages/pgadmin4/pgAdmin4.py

# add an alias to your .bashrc
alias pgadmin4='. /home/<you>/bin/pgadmin4/bin/activate; /home/<you>/bin/pgadmin4/lib/python3.7/site-packages/pgadmin4/pgAdmin4.py'

# you can now start pgadmin4
pgadmin4

# navigate as directed in your browser, e.g. localhost:5050
```

### pgAdmin4 Configuration from Browser

Verify you are in Desktop mode:

* help -> about  # Application Mode should say Desktop

Create a new Server:

* right click on servers -> create

* on the connection tab
  * 127.0.0.1
  * postgres/\<postgres password\>

Chose a name for your postgres server as seen by pgAdmin4 (could be your hostname)

Ensure that your bin path is correct:

* File -> Preferences -> Paths -> Binary Paths -> /usr/bin

#### Create Example Database

Follow instructions at: [Postgres Example DB](http://www.postgresqltutorial.com/load-postgresql-sample-database/)

#### Add SQL Magic to iPython

See: https://github.com/catherinedevlin/ipython-sql

%load_ext sql