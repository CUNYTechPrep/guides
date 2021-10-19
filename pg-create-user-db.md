# How to create users and databases

## Creating Databases for my projects

The postgres server runs in the background and can serve multiple databases for your different projects. Anytime you start a new project, the first thing you'll want to do is setup a database. You can use the following commands to create users and databases using postgres' command line utilities `createuser` and `createdb`.


### `createuser`

While you don't need a separate user for each project, it is a good idea to create separate users. You can do that as follows:

```
$ createuser -P -s -e db_username
```

> This command creates a new postgres user called `db_username` with super privileges and prompts for a password. You can find out about more options using the `man createuser` command.

### `createdb`

Each project will need a separate database. You can create the database as follows:

```
$ createdb -h localhost -U db_username MYAPPNAME_development
```

> This command creates a database named `MYAPPNAME_development` that is owned by `db_username` and can only be accessed via `localhost`

- You should change `MYAPPNAME` to your project name
- It is good practice to add `_development` or `_production` so that we know if the database contains dev data or real data.
- You will need the database _name_, _username_, and _password_ to connect your apps to the database.
