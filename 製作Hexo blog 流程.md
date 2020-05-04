---
slideOptions:
  transition: slide
---

# 製作Hexo blog 流程
## 410613036 生科三 王清瑞

---

- 安裝
首先下載https://nodejs.org/en/
在git Bash 上安裝 Hexo
$ npm install -g hexo-cli

---

- 建blog
$ hexo init blog #建立部落格
$ cd blog #載入資料夾
$ npm install #安裝npm套件
$ npm install hexo-deployer-git --save  //安裝 git 部署套件

---

- 啟動
$ cd blog 
$ hexo server #可以在網站上找到自己的部落格樣板
ctrl+c 結束與部落格的連線，繼續做其他設定

---

- 設定
在資料夾blog中找到"config.yml"
此為網站的配置檔案，可以設定網站標題、作者、作者大頭貼…等
若電腦無法打開該檔案，下載Notepads

---

- 基本資料
title: 網站標題 
subtitle: 網站副標題 
description: 網站描述 
keywords: 網站關鍵字 
author: 作者名稱 
language: zh-TW 
timezone: Asia/Taipei

---

- 主題設置
以NexT為範本
$ cd blog 
$ git clone https://github.com/theme-next/hexo-theme-next themes/next 
#將next的主題資料從github載下來放在next資料夾裡

---

輸入$ hexo generate讓hexo產生靜態檔案
並且輸入$ hexo server來啟動伺服器
在瀏覽器中輸入 localhost:4000 ，可以看見新主題已經成功套用

---

- 與github連結
Github創建一個名稱為ray13036.github.io的repository
打開 config.yml 後，在url 的地方輸入
https://ray13036.github.io/
![](https://i.imgur.com/aZSOcPt.png)


---

- 設定部署至 GitHub 的資訊
一樣在 config.yml，要找到部署至 github 的設定：deploy (在文件的底部)，輸入
![](https://i.imgur.com/KtYdr4T.png)

---

- 連結至github
$ hexo clean  //清除之前建立的靜態檔案
$ hexo generate  //建立靜態檔案
$ hexo deploy  //連結至 Github Pages

---

- 結果
確定完成後，關掉git-bash
在網站上輸入https://ray13036.github.io

---

![](https://i.imgur.com/JL6uXTl.png)


---

- 寫文章
$ hexo new 文章名稱 (會存入sourse裡面的_posts中)
![](https://i.imgur.com/vzLwoQd.png)

---

建議可以把config.yml的中可以將post_asset_folder: false改成true，這樣創建新文章時會建立一個對應資料夾，以放入該文章圖片，好方便管理。
![](https://i.imgur.com/hWsMAK2.png)


---

- 編輯文字
到_posts中找到剛剛建立的markdown檔案，點開進行編輯(記得tag: 後面的空格不能刪掉否則語法會錯誤)
![](https://i.imgur.com/jxqyXZ1.png)

---

錯誤範例
![](https://i.imgur.com/RiYDsJ1.png)

---

編輯完成後，
$ hexo generate 
$ hexo deploy  

---

回部落格，重新整理後
![](https://i.imgur.com/Q9vBzjl.png)


---

THE END

---






