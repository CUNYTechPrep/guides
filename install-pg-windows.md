# Install PostgreSQL on Windows

## Download the installer

There is an interactive installer for Windows that will walk you through installation and setup.

Download the installer here: https://www.postgresql.org/download/windows/

- At this time (October 2022) version 14 is recommended
- Do not install version 15 for CTP projects
- Any version 10-14 should be OK if you already have it pre-installed

## Installation and setup

> **IMPORTANT:** During installation and setup you will be prompted to create multiple new passwords for PostgreSQL itself, for pgAdmin, and for the **postgres** user. Make sure to **save these passwords** as they will be necessary for you to use PostgreSQL.

- Run the installer
    + the default options should work
    + make sure that **pgAdmin** is installed
    + uncheck Stack Builder
        - you **do not need** Stack Builder installed
- Once the installer is done, run **pgAdmin**
    + you can locate this application in your Windows Start Menu
    + the first time you open the app, you will be prompted to create a **master password for pgAdmin** (note this down)
    + for further instructions see the [pgAdmin guide](./pgAdmin-create-user-db.md)

For screenshots of the installation process see this guide: https://www.postgresqltutorial.com/postgresql-getting-started/install-postgresql/