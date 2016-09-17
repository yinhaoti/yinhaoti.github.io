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

## 文件编辑

**1. rm命令**

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

   
## 系统级操作

**1. ln命令**

ln命令用来为文件创件连接，连接类型分为硬连接和符号连接两种，默认的连接类型是硬连接。如果要创建符号连接必须使用"-s"选项。

```ln(选项)(参数)```

```
-s或——symbolic：对源文件建立符号连接，而非硬连接；

--help：在线帮助；
```

- 源文件：指定连接的源文件。如果使用-s选项创建符号连接，则“源文件”可以是文件或者目录。创建硬连接时，则“源文件”参数只能是文件； 
- 目标文件：指定源文件的目标连接文件。

这里主要讲解软连接：
在目录```/usr/liu```下建立一个符号链接文件abc，使它指向目录```/usr/mengqc/mub1```

```
ln -s /usr/mengqc/mub1 /usr/liu/abc 
```

执行该命令后，```/usr/mengqc/mub1```代表的路径将存放在名为```/usr/liu/abc```的文件中。



**NOTICE:**   
删除软连接的时候，只需要删除目标文件：
```
rm -rf file1soft
```

来自: http://man.linuxde.net/ln


