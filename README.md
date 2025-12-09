# 目的

練習使用前端框架暨技術完成 SPA 網站並提供文件整合收集服務



## Roadmap

* 於 GitHub上開啟專案並且利用 GitHub的 內建網站功能作測試
* 建立一個 SPA 網站
* 使用 Git Flow 精神
* 使用純 JavaScript 開發，初期為了能夠滿足畫面條件，可先使用 jQuery
* 與 Firebase整合
* 使用 TypeScript2 提昇 JavaScript 
* 使用 Vue2 框架提昇整體效能並移除 jQuery
* 強烈 MVC 精神
* 使用 less 取代 csss
* 進階功能，例如 RWD (使用 vue-strap 轉譯 bootstrap without jQuery)




### Step 1 建立環境

1. 於 GitHub上開啟 GitHub webpage repository
2. 於本地端新增一個資料夾
3. clong git， 並且 init git flow
4. npm 初始化
5. 為了未來能接上 Vue 框架，所以先安裝 Vue-Cli webpack套件
6. 執行 `npm run build` 讓目前的系統建置一次，產生dist資料夾
7. 先 commit 目前狀態至 all brach 並且 push到 server端看結果
   ![](https://img42.com/j4sT6)
> Code可以從 git tag 0.0.1 reset 回來 (先 fork 回自己專案下)   



### Step 2 網頁樣板開發

說明：
本SPA採用一般傳統三列式網頁開發：上方導覽列，中間內容列，下方版權列

1. 額外下載 Semantic-UI 樣式套件，樣式皆是參考於此
2. 使用 VSCode (Visure Studio Code) 開啟專案資料夾
3. 要額外使用 `npm` 安裝 `style-loader`的方式建置
4. 開始寫 Code


#### Step 2-1 導覽列功能開發

說明：
先針對登入功能完成界面設計

1. 設計導覽列跟登入按鈕
2. 設計按下按鈕後，螢幕會先暗掉並且出現一個表單視窗
3. 按下`註冊`按鈕後會送出資訊
4. 會出現`註冊`後之資訊


#### Step 2-2 主頁面功能開發

說明：
設計主頁面的視覺效果及大綱排版

1. 設計 Glide 幻燈片於導覽列下，並可以輪播圖片
2. 設計三欄卡片欄位，放產品內容


#### Step 2-3 Footer功能開發

說明：
設計 Footer頁面

1. 設計 不同大小欄位，放聯絡方式，版權宣告等   



> 產品詳細頁面待作



### Step 3 簡易註冊/登入後行為

說明：


1. ​