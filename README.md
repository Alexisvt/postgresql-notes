# Notes about PostgreSQL

## How to add `posql` command if windows doesn't recognize it

Add this two paths to environments `PATH`

- C:\Program Files\PostgreSQL\9.6\lib
- C:\Program Files\PostgreSQL\9.6\bin

Change the path route according to your installation folder

## How to connect to the default DB

```cmd
psql -U postgres
```

than will ask the password that you define in the installation process