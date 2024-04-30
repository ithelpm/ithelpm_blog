+++
title = 'Docker-Ch.1'
date = 2024-01-02T15:55:57+08:00
draft = true
+++

## Docker

Docker是一個開放原始碼的開放平臺軟體，可用於部署應用程式

## 為甚麼要Docker?

當我們要部署應程式，我們可能會用到電腦中的某項資源，例如說網路的port就是最為明顯的案例，也是我使用Docker最大的原因。

## 例如說?

以Minecraft作為例子，當我作為一個伺服器主人，我可能有很多朋友，~~但其實沒有~~的時候我可以架設兩個以上的伺服器。

但架設過minecraft的讀者都知道，25565 port一次只能開給一個伺服器，這時候我們的好朋友Docker就登場了!

每當我想建立一個伺服器，我就建立一個Docker container，顧名思義的就是一個容器，mount到一個volume(可想像成硬碟)，在container中執行一個獨立的環境，就像是虛擬機一樣，然後將伺服器的25565 port轉發到伺服器中其他沒有使用的port。

![Mount](https://docs.docker.com/storage/images/types-of-mounts-bind.webp?w=450&h=300)(圖片來源: https://docs.docker.com/storage/bind-mounts/)

上圖是Docker mount的方式，之後可以再另一篇說明。

## 一定要Docker嗎?

當然Docker不是唯一的選擇，例如Podman也是一個類似的東西，不過這個筆者就不熟了。

當然，不一定要用Docker來安裝並應用每個應用程式，如果不嫌麻煩的話，範例中的**多個Minecraft伺服器**就可以分開建立。

只要每次建立的時候點開server.properties改設定就好。
