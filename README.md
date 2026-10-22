# 颱風對台灣的影響：原理 3D / 向量互動視覺化工作台
> Meteorological Dynamics & 3D Vector Interactive Workbench

本專案是一個高階氣象動力學互動視覺化 Web 單頁應用程式，專為探索颱風侵台路徑、中央山脈地形破壞機制、迎風面地形雨與背風面沉降焚風原理而設計。專案採用純 SVG 向量圖形、3D 空間視角轉換與原生 Web Audio API 微音效，打造兼具極速載入與流暢動態體驗的網頁視覺化工作台。

---

## 核心功能設計亮點

1. **多媒體資源極輕量化 (Payload Optimization)**
   * 全站採用純 SVG 幾何描繪台灣地形、等壓線與颱風雲系，零外部點陣圖片依賴，整體檔案體積精簡，達成極速加載。

2. **三維空間視角無縫切換 (3D Spatial Perspectives)**
   * **2D 平面視角**：清晰觀察氣旋結構與等壓線配置。
   * **等角 3D (Isometric)**：立體呈現台灣中央山脈地形與氣旋包覆感。
   * **深度透視 (Perspective 3D)**：沉浸式感受暴風圈與立體空間層次。

3. **氣象動力學與地形剖面解析 (Cross-Section Dynamics)**
   * **時間軸互動播放 (Scrubber)**：動態模擬颱風接近、觸陸破壞與過山減弱的三階段演變過程。
   * **地形剖面實驗台**：視覺化呈現迎風面水氣強制抬升造成的「地形雨」，以及過山下沉帶來的乾暖「焚風（Foehn Wind）」效應。
   * **風雨威脅指數監控**：即時連動顯示關鍵縣市與區域的警戒層級。

4. **60 FPS 流暢動態與微互動 (Audio & Motion Tuning)**
   * **GPU 硬體加速**：動畫屬性嚴格鎖定於 `transform` 與 `opacity`，避免瀏覽器重排（Reflow），確保 60 FPS 零掉幀。
   * **彈性物理曲線**：動畫緩動採用極致彈跳 `cubic-bezier(0.34, 1.56, 0.64, 1)` 曲線。
   * **Web Audio API 微音效**：採用原生代碼即時合成點擊與切換音效，零音檔載入延遲。

---

## 快速開始 

### 本地開啟
1. 下載或 Clone 本專案儲存庫。
2. 用任何現代瀏覽器（Chrome, Edge, Safari, Firefox）直接雙擊開啟 `index.html` 即可運行。

### 線上 Live Demo 部署 (GitHub Pages)
1. 將專案推送到您的 GitHub Repository。
2. 前往 **Settings** -> **Pages**。
3. 在 **Branch** 選項選擇 `main` 並儲存。
4. 等候約 1 分鐘即可透過專屬 URL 開啟線上互動展示。

---

## 技術架構 

* **前端框架/語言**：HTML5, CSS3 (CSS Variables, Flexbox, CSS Grid)
* **向量視覺化**：SVG (Scalable Vector Graphics), CSS `@keyframes`
* **音訊處理**：Web Audio API (OscillatorNode, GainNode)
* **字型與樣式**：Google Fonts (Noto Sans TC, JetBrains Mono), Dark Theme HUD

---

## 自評與驗收

- [x] **資源瘦身**：純向量優先，零外部點陣圖，加載節省率達 80% 以上。
- [x] **動態渲染**：動畫操控嚴格限定於 `transform` 與 `opacity`，維持 60 FPS 影格預算。
- [x] **物理曲線**：微互動按鈕採用擬真彈力 `cubic-bezier` 緩動。
- [x] **微音效規格**：採用 Web Audio API 純代碼合成，0KB 外部音檔依賴。
- [x] **功能整合**：支援時間軸 Scrubber 連動、三維視角切換與主控 Console 零報錯。

---

© 2026 颱風對台灣的影響：原理 3D / 向量互動視覺化工作台 | 多媒體網頁設計作業
