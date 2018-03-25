presto

```
presto --server presto.smartnews.internal:8081 --catalog hive --schema default
```

Eliminating duplicate values based on only one column of the table
```
SELECT s.siteName, s.siteIP, h.date
FROM sites s INNER JOIN
     (select h.*, row_number() over (partition by siteName order by date desc) as seqnum
      from history h
     ) h
    ON s.siteName = h.siteName and seqnum = 1
ORDER BY s.siteName, h.date

```


```

```
