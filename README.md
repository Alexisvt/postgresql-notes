# Notes about PostgreSQL CLI (psql command-line tool)

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

## How to describe a table

```cmd
\d+ tablename
```

**Note**: We need to run this command in the `psql` command-line tool

## How to run an external sql script file to your database

```cmd
psql -U username targetDataBase < C:\path-to-your-sql-script\script-to-apply.sql
```

## How to enable logs in Postgres (Windows SO)

First we need to go to `data` folder in **Postgres** installed directory and edit `postgresql.conf` file, add this two lines:

```txt
log_statement = 'all'
log_min_duration_statement = 0
```

**Reference**: [How to enable logging in Postgresql 9.2 and 9.1](http://sharadchhetri.com/2013/12/08/how-to-enable-logging-in-postgresql-9-2-and-9-1/)

Then we need to restart the server using this command

```cmd
pg_ctl -D "C:\Program Files\PostgreSQL\9.6\data" restart
```

**Note**: Change the directory according to yours installed Postgres version.

After doing those steps all the logs will be register into `pg_log` folder inside `data` of **Postgres** installation, sample dir:

```txt
C:\Program Files\PostgreSQL\9.6\data\pg_log
```