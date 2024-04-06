# How to export your vivaldi history

```
% cd "/Users/patrickhochstenbach/Library/Application Support/Vivaldi/Default"
% sqlite3 History
SQLite version 3.32.3 2020-06-18 14:16:19
Enter ".help" for usage hints.
sqlite> .headers on
sqlite> .mode csv
sqlite> .output /tmp/my-history.csv
sqlite> SELECT datetime(last_visit_time/1000000-11644473600,'unixepoch','localtime'), url FROM urls ORDER BY last_visit_time DESC
```

## See also

https://github.com/Stefan-Heimersheim/browser_tools/tree/master
