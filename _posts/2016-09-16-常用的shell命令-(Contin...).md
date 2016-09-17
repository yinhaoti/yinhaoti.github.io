---
layout:     post
title:      "常用的shell命令 (Conti...)"
subtitle:   ""
date:       2016-09-16
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - Shell 
    - 备忘
---

### 文件编辑

1. rm命令

   ```
   rm [选项] 文件… 
   ```

   >删除一个目录中的一个或多个文件或目录，如果没有使用- r选项，则rm不会删除目录。如果使用 rm 来删除文件，通常仍可以将该文件恢复原状。
   

   ​
   -r, -R, --recursive   指示rm将参数中列出的全部目录和子目录均递归地删除。
   
   -f, --force    忽略不存在的文件，从不给出提示。

   常用例子：

   ```shell
   rm -r pictire ## delete all files inside directory of picture
   ```

   ​