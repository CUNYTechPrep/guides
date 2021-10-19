# Install PostgreSQL on Ubuntu

## Installing on Ubuntu 20.04

On Ubuntu 20.04 you can install postgres with the following commands:

```
$ sudo apt update
$ sudo apt install postgresql postgresql-contrib
```

### Setup your linux user as a DB user

On Ubuntu, you *may* have to make a postgresql user that matches your Ubuntu username.

Run these commands **ONCE** (replace `UBUNTU_USERNAME` with your own username):

```
sudo su - postgres
createuser -P -s -e UBUNTU_USERNAME
exit
```

> After this one time step, you wont need the sudo commands to create more databases and database users.
