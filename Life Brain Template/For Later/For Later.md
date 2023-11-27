# Read Later

```dataview
TABLE file.ctime AS "Created On", file.mtime AS "Last Updated"
FROM "For Later/Read Later" OR #todo/read 
WHERE file.name != "tags note"
SORT file.name ASC
LIMIT 10
```

# Watch Later

```dataview
TABLE file.ctime AS "Created On", file.mtime AS "Last Updated"
FROM "For Later/Watch Later" OR #todo/read 
WHERE file.name != "tags note"
SORT file.name ASC
LIMIT 10
```

# Listen Later

```dataview
TABLE file.ctime AS "Created On", file.mtime AS "Last Updated"
FROM "For Later/Listen Later" OR #todo/read 
WHERE file.name != "tags note"
SORT file.name ASC
LIMIT 10
```

# Learn Later

```dataview
TABLE file.ctime AS "Created On", file.mtime AS "Last Updated"
FROM "For Later/Learn Later" OR #todo/read 
WHERE file.name != "tags note"
SORT file.name ASC
LIMIT 10
```

---
