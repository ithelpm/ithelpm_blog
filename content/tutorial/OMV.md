+++
title = '甚麼是Open Media Vault?(文長)'
date = 2024-03-19T09:39:29+08:00
draft = true
tags = ['OMV', 'Linux', 'NAS']
+++
在這篇文章中，將會介紹各種筆者已經用過的OMV套件、功能等等。

# Open Media Vault!
Open Media Vault以下簡稱OMV

OMV是一個NAS作業系統，

NAS則是Network Attached Storage的縮寫，用來透過網路進行資料存儲。

當然我相信對OMV有興趣的人應該對NAS不陌生，所以如果有人想知道NAS是甚麼的話可以留言詢問，或是等筆者在另外寫一篇文章。

## 關於OMV的架構

OMV是一個基於Debian Linux的系統，也就是說他其實和Ubuntu很像，很多套件相通，其中就包含知名的Docker。

Docker可以迅速的建立App，再搭配portainer更是~~絕配~~!

## Why OMV

每當我們討論到一個軟體、硬體或任何東西，我們都可以問一個問題:為甚麼要用這個XXXX。

那我們為甚麼要用OMV? 有替代品嗎?

答案是**有**，例如說Synology(付費)、TrueNAS(免費開源)，我們為甚麼不用他們?

這真的比較偏向喜好問題，首先Synology"**通常**"需要付費購買硬體設備，TrueNAS筆者用過的心得是太複雜，更新後很多教學文都沒改等等，實在是勸退人。

不過還有個原因是因為之前眼睛一黑買了硬碟塔，跟NAS硬碟，結果發現TrueNAS似乎不太支援外接硬碟，所以心灰意冷的換了OMV。

## OMV怎麼用?

首先要講到安裝，關於安裝就有請[官方文件](https://docs.openmediavault.org/en/latest/installation/index.html)。

官網是英文，如果讀者有問題的話可以從上面的官方文件找，或是留言詢問。

### 安裝準備:

1. ![USB](../../USB1.png)
2. 下載OMV的ISO檔[官方下載點](https://www.openmediavault.org/?page_id=77)
3. 燒錄軟體，這邊推薦[Rufus](https://rufus.ie/zh_TW/)-僅支援windows作業系統

接下來將iso燒錄到USB中，準備就完成了!

接下來就跟安裝作業系統一樣，準備一台電腦當作伺服器

#### 這邊注意可以不用讀顯

大部分的伺服器是透過網路存取，所以幾乎不需要顯示。但筆者我比較誇張，用的是AMD的CPU，所以連內顯都沒有，第一次安裝的時候還要拔GPU到伺服器上，十分不推薦，所以可以用Intel的CPU。

筆者我的伺服器配備如下:

 - Ryzen 5 5600x
 - 32G RAM
 - 256G ssd+ 4T NAS HDD/1T HDD

就這樣...<br />
沒錯，就這樣!<br />

身為一台NAS，他最重要的當然是存儲，所以硬碟比較重要，因為筆者是拿換下來的電腦來作為NAS的伺服器，所以CPU/RAM才配得比較好。

通常可以不用特地去買配備組伺服器，像筆者一樣用舊電腦的人不佔少數。

### 安裝OMV

接下來要安裝OMV。

1. 插入USB
2. 開機，進入BIOS
3. 選擇你的USB作為開機硬碟

接下來要進入OMV安裝程序後會出現選項:

![install](../../install_1.png)

請選擇**Install**<br />
接下來會讓你選擇安裝程序中要使用的語言

![lang](../../install_2.png)

這邊因為是從官方文件上~~借來用的~~關係所以先選英文，地區則是選US

![location](../../install_3.png)

鍵盤配置:

![keymap](../../install_4.png)

接下來等他讀條跑完後會出現設定裝置名稱，網路等的設定，如果不知道怎麼設定，**請一律Enter**。

![device name](../../install_7.png)

![internet](../../install_8.png)

接下來要設定你的密碼，這是用來SSH的密碼，不是workbench的。

![pass](../../install_9.png)

![veri](../../install_10.png)

關於這個稍後會解釋。

最後設定時區和作業系統的硬碟(推薦SSD)

![TZ](../../install_11.png)

![os disk](../../install_12.png)

最後的最後選擇離你所在地最近的地區以完成系統第一次的下載&更新。

![zone](../../install_14.png)

這個選第一個:

![site](../../install_15.png)

然後讀完條，重開機後**拔USB**就完成了

![](../../install_19.png)
