
````markdown
# 日幣匯率計算器

這是一個適合在 iPhone Safari 使用的日幣匯率計算器。

可以自動抓取今日 **JPY → TWD** 匯率，輸入日幣價格後，自動換算成台幣，並套用固定倍率與加價金額。

## 功能特色

- 自動抓取今日日幣兌台幣匯率
- 可手動修改匯率
- 輸入日幣金額後即時計算台幣
- 固定倍率預設為 `1.05`
- 可快速選擇加價金額：
  - 0
  - 50
  - 80
  - 100
  - 120
  - 150
- 可自訂加價金額
- 支援深色模式 Dark Mode
- 可複製計算結果
- 支援 iPhone Safari 加入主畫面
- 使用 `localStorage` 儲存上次輸入內容

## 計算公式

```text
台幣金額 = 日幣價格 × JPY/TWD 匯率 × 固定倍率 + 加上金額
````

預設倍率為：

```text
1.05
```

範例：

```text
日幣價格：10,000
匯率：0.215
倍率：1.05
加上金額：100

計算結果 = 10,000 × 0.215 × 1.05 + 100
```

## 使用方式

### 1. 直接開啟網頁

如果已經部署到 GitHub Pages，可以用 Safari 開啟網址：

```text
https://你的GitHub帳號.github.io/jpy-calculator/
```

### 2. 加入 iPhone 主畫面

1. 用 iPhone 的 Safari 開啟計算器網址
2. 點下方的分享按鈕
3. 選擇「加入主畫面」
4. 名稱可設定為「日幣計算器」
5. 點選「新增」

之後就可以像 App 一樣從 iPhone 主畫面開啟。

## GitHub Pages 部署方式

### 1. 建立 Repository

建立一個 GitHub repository，例如：

```text
jpy-calculator
```

### 2. 上傳檔案

請確保主要 HTML 檔案命名為：

```text
index.html
```

如果有自訂 iPhone 主畫面圖示，請一起上傳：

```text
apple-touch-icon.png
```

建議專案結構如下：

```text
jpy-calculator/
├── index.html
├── apple-touch-icon.png
└── README.md
```

### 3. 開啟 GitHub Pages

進入 repository 後：

1. 點選 `Settings`
2. 左側選擇 `Pages`
3. Source 選擇 `Deploy from a branch`
4. Branch 選擇 `main`
5. Folder 選擇 `/root`
6. 點選 `Save`

完成後 GitHub 會產生網站網址。

## iPhone 主畫面圖示

若要自訂 iPhone 主畫面圖示，請準備一張 PNG 圖片：

```text
180 × 180 px
```

檔名建議為：

```text
apple-touch-icon.png
```

並在 `index.html` 的 `<head>` 中加入：

```html
<link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
<meta name="apple-mobile-web-app-title" content="日幣計算器">
<meta name="apple-mobile-web-app-capable" content="yes">
```

如果之前已經加入過主畫面，請先刪除舊圖示，再重新用 Safari 加入主畫面。

## 匯率來源

本工具使用公開匯率 API 抓取 JPY → TWD 匯率。

如果匯率抓取失敗，仍可手動輸入匯率後繼續計算。

## 注意事項

* 匯率僅供估算使用，實際刷卡、換匯或銀行牌告匯率可能不同
* 使用 iPhone「檔案 App」直接開啟 HTML 時，部分功能可能無法正常執行
* 建議部署到 GitHub Pages 後，用 Safari 開啟使用
* 若 API 無法連線，請手動輸入匯率

## License

此專案可自由修改與自用。
