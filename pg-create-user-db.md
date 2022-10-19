# How to create users and databases with the command line

## Creating Users and Databases for PostgreSQL projects

The PostgreSQL server runs in the background and can serve multiple databases for your different projects. Anytime you start a new project, the first thing you'll want to do is setup a database. You can use the following commands to create users and databases using the command line utilities `createuser` and `createdb`.

> NOTE: to use these command line utilities the operating system PATH variable needs to be updated to include the PostgreSQL bin folder. Installation using `brew` or `apt` does this automatically. If you installed using a graphical installer you may have to update the PATH environment variable manually. ([see here for Windows](https://blog.sqlbackupandftp.com/setting-windows-path-for-postgres-tools))

### `createuser`

Although you don't need a separate user for each project, it is a good idea to create separate users. You can do that as follows:

```
$ createuser -P -s -e db_username
```

> This command creates a new PostgreSQL user called `db_username` with super privileges and prompts for a password. You can find out about more options using the `man createuser` command.

### `createdb`

Each project will need a separate database. You can create the database as follows:

```
$ createdb -h localhost -U db_username MYAPPNAME_development
```

> This command creates a database named `MYAPPNAME_development` that is owned by `db_username` and can only be accessed via `localhost`

- You should change `MYAPPNAME` to your project name
- It is good practice to add `_development` or `_production` so that we know if the database contains dev data or real data.
- You will need the database _name_, _username_, and _password_ to connect your apps to the database.
