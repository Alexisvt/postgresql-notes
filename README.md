# Notes about PostgreSQL

## How to add `posql` command if windows doesn't recognize it

Add this two paths to environments `PATH`

- C:\Program Files\PostgreSQL\9.6\lib
- C:\Program Files\PostgreSQL\9.6\bin

Change the path route according to your installation folder

## How to connect to postgres using already defined user

```cmd
psql -U username
```

Where `username` is the one that you want to use to connect to Postgres

than will ask the password that you define in the installation process

## How to create a new newdatabase

```cmd
createdb -U postgres newdatabase
```

Then you need to type the password for the `postgres` user

## How to access to a DB using commands

```cmd
psql -U username databasename
```

Then you need to type the password for `username`

## How to list all the Databases in PostgreSQL

```cmd
> \l
```

**Note**: in order to run this command you need to be connect to postgres

## How to show the list of tables

```cmd
database=# \dt
```

you first need to connect to the desire database and then type `\dt` command

## How to run an external sql script file to your database

```cmd
psql -U username targetDataBase < C:\path-to-your-sql-script\script-to-apply.sql
```

