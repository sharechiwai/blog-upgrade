---
title: Prisma Output SQL query
date: 2022-06-27T01:38:21.414Z
draft: false
featured: false
categories:
  - Prisma
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
轉左用 `NodeJs` 之後就發現 `Entity Framework` 有多好\
之前用 `EF` 很方便便可以知道 `EF Generate` 果條
係**Prisma** 度點先可以`Log` 到條`query` 呢?

**解決方便**
我們只需要在declare Prisma Client 時加上 log query 這個 parameter 便可:

```javascript
const prisma = new PrismaClient({ log: ['query'] });
```

Hope you find it useful