# Daily Routine
```dataview
TABLE WITHOUT ID
file.link AS "Weekly",
🥊Training AS "🥊Training",
💼Program AS "💼Program",
🖥️Leetcode AS "🖥️Leetcode"
FROM "Daily Notes"
SORT file.ctime DESC
LIMIT 7
```

---

```dataview
TABLE WITHOUT ID
file.link AS "Monthly",
🥊Training AS "🥊Training",
💼Program AS "💼Program",
🖥️Leetcode AS "🖥️Leetcode"
FROM "Daily Notes"
SORT file.ctime DESC
LIMIT 30
```

---
# Active Projects

```dataview
TABLE WITHOUT ID 
file.link AS "Projects",
project_status AS "Status",
project_overview AS "Overview"
FROM #project 
WHERE file.name != "Project Template" AND project_status != "✅ Completed"
SORT choice(project_status = "⌛ In Progress", 1, choice(project_status = "📋 Not Started", 2, choice(project_status = "✅ Completed", 3, "other"))), file.name ASC
```

# Completed Projects

```dataview
TABLE WITHOUT ID 
file.link AS "Projects",
project_status AS "Status",
project_overview AS "Overview"
FROM #project 
WHERE project_status = "✅ Completed"
SORT choice(project_status = "⌛ In Progress", 1, choice(project_status = "📋 Not Started", 2, choice(project_status = "✅ Completed", 3, "other"))), file.name ASC
```

---
# Read Later
```dataview
TABLE 
FROM "For Later/Read Later"
SORT file.link ASC
LIMIT 10
```

---