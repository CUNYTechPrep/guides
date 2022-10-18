# Install PostgreSQL on Mac

## Installing with Homebrew

The easiest way to install postgres on the Mac is using Homebrew with the following commands:

```
brew update
brew install postgresql@14
```

### Starting up the server

After installing postgres, you need to turn it on before you can begin using it. There are a few ways to do that, but the easiest is using the homebrew services manager. You can set that up as follows:

First, install brew services if you don't already have it installed:

```
brew tap homebrew/services
```

Next, ensure that the postgres server is started with the following command.

```
brew services start postgresql
```

## Other helpful commands to know

You can start, stop, or restart the postgres server with the following commands:

For starting it up:

```
brew services start postgresql
```

For stopping the server:

```
brew services stop postgresql
```

To restart the server run:

```
brew services restart postgresql
```
