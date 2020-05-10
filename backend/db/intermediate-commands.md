# advanced SQL

## where **"=" multiple values**

`SELECT ... FROM ... WHERE something IN ('one','two',3,4)`

`SELECT key,list_count,ws_sentiment FROM data.words WHERE key IN ('submissions','indications','motions','hint','allusions','clues');`

## replace

`Use SELECT to display replaced value. Remove when using in SQL query.`

`SELECT REPLACE(REPLACE(REPLACE((SELECT list FROM data.words WHERE key='wordy'), '[',''),']',''),'"','''')`

## function: substr \(cut off first 3 characters\)

`ALTER TABLE data.words ALTER COLUMN pos1 TYPE varchar(3) USING substr("pos1", 1, 3)`
