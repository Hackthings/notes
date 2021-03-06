---
description: '*** on Ubuntu 18, Postgres v 12 ***'
---

# backup / restore

## First, on local: **Copy backup file to server:**

`scp /srv/data-08-26.sql root@142.93.251.57:/tmp/data.sql`

## **Restore schema only \(no data\):**

`pg_restore --host "localhost" --port "5432" --username "postgres" --dbname "words" --verbose "/tmp/db-backup-july.sql"`

prepend `PGPASSWORD=xxx` to set password programmatically

## **Restore database on Linux server:**

### **Restore specific schema:**

**FIRST,**  
`sudo -i -u postgres`, `psql words`, `DROP SCHEMA data CASCADE;`**, don't leave out the semicolon!**  
Wait for confirmation response "DROP SCHEMA".

**THEN,**  
`CREATE SCHEMA data AUTHORIZATION nodejs;`**, again, don't leave out the semicolon!**  
Wait for confirmation response "DROP SCHEMA".

**THEN,**  
`\q`, don't forget this bit!  
`pg_restore --host "localhost" --port "5432" --username "postgres" --dbname "words" --verbose --schema "data" "/tmp/data.sql"`

**TODO:**  
Try `--delete --create` flags and do same on `pg_dump` on CLI. Don't use PgAdmin.

Enter password when prompted, and done!

## **MacOS PgAdmin4 v 11...**

**Backup specific schema:**`pg_dump --file "/www/words.crawl.sql" --host "localhost" --port "7777" --username "postgres" --no-password --verbose --format=c --blobs --schema "crawl" "words"`

\*\*\*\*

## **MacOS PgAdmin4 v 12...**

**Backup specific schema:**  
`pg_dump --file "/www/words.data.sql" --host "localhost" --port "5432" --username "postgres" --no-password --verbose --format=c --blobs --schema "data" "words"`

**Restore specific schema:**  
\(Must drop-cascade tables first\)  
`pg_restore --host "localhost" --port "5432" --username "postgres" --no-password --dbname "words" --verbose --schema "data" "/www/words.data.sql"`

