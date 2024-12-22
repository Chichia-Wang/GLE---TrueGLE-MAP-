# 美食TrueGLE Map - 智慧餐廳評論分析系統

這是一個結合 Google Maps 評論爬蟲與 AI 分析的智慧餐廳評論系統，能夠自動收集、分析並提供完整的餐廳評價報告。

## 功能特色

- 🔍 即時爬取 Google Maps 評論
- 🤖 AI 智慧分析評論內容
- 📊 自動產生餐廳優缺點分析
- 🍽️ 推薦必點菜品整理
- 💯 綜合評分與總結報告

## 技術架構

### 前端技術
- React 18.3
- Vite 6.0
- Tailwind CSS
- Lucide React (圖標庫)

### 後端技術
- Python Flask
- Selenium WebDriver
- OpenAI GPT-4
- PEFT (Parameter-Efficient Fine-Tuning)
- Transformers (BERT-based QA Model)

## 系統需求

- Node.js >= 18.0.0
- Python >= 3.8
- Chrome 瀏覽器

## 安裝說明

1. 克隆專案
```bash
git clone [your-repository-url]
```

2. 安裝前端依賴
```bash
cd restaurant-app
npm install
```

3. 安裝後端依賴
```bash
cd scraper
pip install -r requirements.txt
```

4. ChromeDriver 設定（重要）

根據您的 Chrome 瀏覽器版本下載對應的 ChromeDriver
將 ChromeDriver 放置在專案的正確位置：
- ChromeDriver 檔案結構應如下：

chromedriver-win32/

├── chromedriver.exe

├── LICENSE.chromedriver

└── THIRD_PARTY_NOTICES.chromedriver

chromedriver-win64/

├── chromedriver.exe

├── LICENSE.chromedriver

└── THIRD_PARTY_NOTICES.chromedriver

- 請確保下載後的 ChromeDriver 檔案完整性，包含執行檔和授權文件
- 將完整的 ChromeDriver 資料夾放置在 scraper 目錄下
- 注意：請選擇與您系統架構相符的版本（32位元或64位元）


5. API KEY設定

你可以在此處直接更換成您的API KEY：
```
# 設定 OpenAI API Key
client = OpenAI(api_key="輸入您的api key")
```

但為了安全性考量，建議您直接在後端目錄建立 .env 檔案
```
OPENAI_API_KEY=your_api_key
```

## 啟動專案

### 啟動前端服務

```bash
Copycd restaurant-app
npm run dev
```

### 啟動後端服務

```bash
Copycd scraper
python app.py
```

### 使用說明

1. 在搜尋框輸入欲查詢的餐廳名稱
2. 系統會自動爬取該餐廳的 Google Maps 評論
3. AI 模型會分析評論內容，生成分析報告
4. 查看餐廳的優缺點、推薦菜品及總體評價

### 開發注意事項

* 確保 ChromeDriver 版本與本地 Chrome 瀏覽器版本相符
* 前端開發時注意 Tailwind CSS 的使用規範
* 後端開發時需注意 API 呼叫限制和爬蟲間隔
* AI 模型訓練和更新需要足夠的運算資源

## 授權說明
本專案採用 MIT 授權條款

## 貢獻指南
歡迎提交 Pull Request 或建立 Issue 來改善專案

## 技術支援
如有任何問題，請聯繫專案維護者或建立 Issue

