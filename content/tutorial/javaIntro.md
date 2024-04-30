+++
title = 'Java Intro'
date = 2024-03-12T13:47:16+08:00
draft = true
tags = ['Java', 'Programming', 'Tutorial']
+++

在此分類中將會介紹關於Java的細節，其中會用標題分類，可用``shift+f``搜尋。

## Java中有嚴謹的語法限制

以python舉例:

```<!-- language:python -->
print()
```

在Java中則是:

```<!-- language:java-->
System.out.println();
```

其中System代表整個系統，out是指output stream，println則是將括號內個字串放入output stream。

輸入的對比如下:

```<!--  language:python -->
input()
```

```<!-- language:java -->
Scanner sc = new Scanner(System.in);
sc.next();
```

有人會問，這麼麻煩，學他幹嘛!

### 這就要看它的用途了

## Java通常用於伺服器、跨平台軟體

常舉的例子有:

Spring ![Spring Icon](../../Spring_Framework-Logo.wine.svg)

Minecraft ![Minecraft Icon](../../minecraft_logo_icon_168974.svg)

不過也不僅限於這些用途。

Java有許多框架，例如JavaFX、awt、swing和JavaX，還有做為其替代的Kotlin語言。

甚至Kotlin中也可以直接``import`` Java的package，所以學習Java也並不是沒有好處的。
