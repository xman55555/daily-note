---
title: sessionStroage应用要点
date: 2018-11-08 04:10:03
tags: [开发笔记, JS]
---

* #### 基本使用

  ```js
  sessionStorage.setItem( key, value);
  ```


* #### sessionStorage 的使用注意事项:

  > sessionStorage 不能将对象、数组等格式的数据作为 value 进行存储

1. 如果存储对象、数组等格式的数据，需要将数据格式转为字符串格式，然后进行存储

   ```js
   sessionStorage.setItem( key, JSON.stringify(myData));
   ```

2. · 使用时直接从 sessionStorage 中获取：

   ```js
   const myData = JSON.parse(sessionStorage.getItem(key) || null);
   ```


