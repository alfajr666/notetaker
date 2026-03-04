---
title: Market Intelligence Hub
---

# 🧠 Market Intelligence Hub

## 📥 Research Inbox
```dataview
LIST
FROM "Market_Intelligence/10_Research_Library"
WHERE status = "Raw"
SORT announce_date DESC


TABLE confidence, horizon
FROM "Market_Intelligence/20_Decision_Journal"
WHERE status = "Open"


LIST
FROM "Market_Intelligence/30_Themes"
WHERE status = "Active"
