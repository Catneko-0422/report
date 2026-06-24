---
marp: true
theme: gaia
_class: lead
paginate: true
header: ' '
footer: '← 回選單'
transition: fade 0.35s
style: |
  section {
    font-family: 'Noto Sans TC', 'Segoe UI', sans-serif;
    background-color: #1e1e2e;
    background-image: url('./assets/background.jpg');
    background-size: cover;
    background-position: center;
    padding: 50px 60px 50px 80px;
    color: #cdd6f4;
  }

  section::before {
    content: "";
    position: absolute;
    inset: 28px;
    background:
      linear-gradient(180deg, #89b4fa, #cba6f7, #f38ba8) left / 4px 80% no-repeat,
      rgba(24, 24, 37, 0.72);
    backdrop-filter: blur(14px) saturate(160%);
    -webkit-backdrop-filter: blur(14px) saturate(160%);
    border: 1px solid rgba(255, 255, 255, 0.09);
    border-radius: 22px;
    box-shadow:
      0 8px 40px rgba(0, 0, 0, 0.80),
      inset 0 1px 0 rgba(255, 255, 255, 0.06);
    z-index: 0;
  }

  /* 確保所有內容浮於遮罩卡片之上 */
  section > * { position: relative; z-index: 1; }

  /* ── 多種動畫效果 ── */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-16px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(14px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeLeft {
    from { opacity: 0; transform: translateX(-18px); }
    to   { opacity: 1; transform: translateX(0); }
  }
  @keyframes scaleIn {
    from { opacity: 0; transform: scale(0.92); }
    to   { opacity: 1; transform: scale(1); }
  }
  @keyframes blurIn {
    from { opacity: 0; filter: blur(4px); }
    to   { opacity: 1; filter: blur(0); }
  }

  /* ── 元素各自不同動畫 ── */
  section > *:not(img) {
    animation: fadeUp 0.45s ease-out both;
  }
  section h1, section h2 {
    animation: fadeDown 0.5s ease-out both;
  }
  section h3 {
    animation: scaleIn 0.4s ease-out both;
  }
  section table {
    animation: scaleIn 0.5s ease-out both;
  }
  section blockquote {
    animation: fadeLeft 0.45s ease-out both;
  }
  section code {
    animation: blurIn 0.4s ease-out both;
  }

  /* 加上 no-fade class 的 slide 關閉所有動畫 */
  section.no-fade > * {
    animation: none !important;
  }

  section > *:nth-child(2) { animation-delay: 0.06s; }
  section > *:nth-child(3) { animation-delay: 0.12s; }
  section > *:nth-child(4) { animation-delay: 0.18s; }
  section > *:nth-child(5) { animation-delay: 0.24s; }
  section > *:nth-child(6) { animation-delay: 0.30s; }
  section > *:nth-child(7) { animation-delay: 0.36s; }

  /* ── 引言區塊樣式 ── */
  blockquote {
    border-left: 4px solid #cba6f7;
    background: rgba(203, 166, 247, 0.08);
    padding: 12px 20px;
    border-radius: 0 10px 10px 0;
    margin: 0.8em 0;
  }
  blockquote p { color: #cdd6f4; font-style: italic; }

  h1 {
    color: #89b4fa;
    font-size: 1.75em;
    font-weight: 700;
    text-shadow: 0 0 14px rgba(137, 180, 250, 0.40);
    margin-bottom: 0.3em;
  }

  h2 {
    color: #a6e3a1;
    font-size: 1.35em;
    font-weight: 600;
    padding-bottom: 8px;
    margin-bottom: 0.7em;
    position: relative;
  }
  h2::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    width: 60px;
    height: 3px;
    background: linear-gradient(90deg, #a6e3a1, #89b4fa);
    border-radius: 2px;
  }

  h3 {
    color: #f9e2af;
    font-size: 1.05em;
    font-weight: 500;
    margin: 0.5em 0 0.25em;
  }

  p, li {
    font-size: 21px;
    line-height: 1.75;
    color: #bac2de;
  }

  /* strong 改為 Catppuccin Mauve，在深色背景更醒目 */
  strong {
    color: #cba6f7;
    font-weight: 600;
  }

  /* ── 標題頁專屬樣式 ── */
  section.lead { text-align: center; }

  section.lead h1 {
    font-size: 2.4em;
    color: #fab387;
    line-height: 1.2;
    text-shadow: 0 0 20px rgba(250, 179, 135, 0.35);
  }

  section.lead h2 {
    border: none;
    color: #b4befe;
    font-size: 1.15em;
    font-weight: 400;
    margin-top: 0;
  }

  section.lead p {
    color: #a6adc8;
    font-size: 20px;
    line-height: 2.2;
  }

  /* ── 表格 ── */
  table {
    border-collapse: collapse;
    width: 100%;
    margin-top: 0.5em;
    font-size: 20px;
    position: relative;
    z-index: 1;
  }

  th {
    background: rgba(137, 180, 250, 0.14);
    color: #89b4fa;
    font-weight: 600;
    padding: 10px 18px;
    border: 1px solid rgba(255, 255, 255, 0.08);
    text-align: center;
  }

  td {
    padding: 9px 18px;
    border: 1px solid rgba(255, 255, 255, 0.05);
    color: #bac2de;
    vertical-align: middle;
  }

  tr:nth-child(even) td {
    background: rgba(255, 255, 255, 0.03);
  }

  tr:hover td {
    background: rgba(137, 180, 250, 0.08);
    transition: background 0.25s ease;
  }

  /* ── 行內程式碼標籤 ── */
  code {
    background: rgba(243, 139, 168, 0.18);
    color: #f38ba8;
    padding: 3px 10px;
    border-radius: 8px;
    font-size: 0.86em;
    font-weight: 500;
    letter-spacing: 0.01em;
  }

  /* ── 角色圖片位置基底 ── */
  .char-r, .char-l, .char-toc-r {
    position: absolute;
    z-index: 2;
  }

  /* 目錄頁角色 (character.png) */
  .char-toc-r {
    top: 50%;
    transform: translateY(-50%);
    height: 100%;
    right: 65px;
  }
  .char-toc-r { right: -0px }

  /* 案例頁角色 (character-atri.png) */
  .char-r {
    top: 80%;
    transform: rotate(-10deg) translateY(-50%);
    height: 150%;
  }
  .char-r { right: -380px; }
  .char-l { left: 40px; }

  /* ── 背景裝飾圖片（放在角色後面） ── */
  .char-bg-r, .char-bg-l {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    height: 85%;
    z-index: 1;
    opacity: 0.95;
  }
  .char-bg-r { right: 45px; }
  .char-bg-l { left: 10px; }

  /* 小型裝飾角色（SD 貼圖，放在角落不佔主要空間） */
  .char-deco {
    position: absolute;
    z-index: 1;
    bottom: 15px;
    right: 25px;
    height: 32%;
    opacity: 0.80;
    pointer-events: none;
    filter: drop-shadow(0 2px 8px rgba(0,0,0,0.4));
  }
  .char-deco-l {
    left: 25px;
    right: auto;
  }

  /* 有角色圖片的 slide 自動縮減文字寬度避免重疊 */
  section:has(.char-r, .char-bg-r, .char-toc-r) {
    padding-right: 450px;
  }
  section:has(.char-l, .char-bg-l) {
    padding-left: 450px;
  }

  .text-right { text-align: right !important; }

  /* ── 結尾感謝頁 ── */
  section.thanks {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  section.thanks h1 {
    color: #fab387;
    font-size: 2.4em;
    text-shadow: 0 0 20px rgba(250, 179, 135, 0.35);
    margin-bottom: 0.2em;
  }
  section.thanks p {
    color: #a6adc8;
    font-size: 22px;
  }
  .thanks-gif {
    height: 280px;
    margin-top: 20px;
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.5);
  }

  /* ── 可愛下一頁箭頭 ── */
  @keyframes arrowBounce {
    0%, 100% { transform: translateY(0); opacity: 0.5; }
    50%      { transform: translateY(8px); opacity: 1; }
  }
  .next-arrow {
    position: absolute;
    bottom: 18px;
    right: 50%;
    transform: translateX(50%);
    font-size: 28px;
    color: #89b4fa;
    animation: arrowBounce 1.6s ease-in-out infinite;
    z-index: 2;
    text-shadow: 0 2px 12px rgba(137, 180, 250, 0.35);
    pointer-events: none;
    opacity: 0.7;
  }

  /* ── 頁碼 (由 Marp ::after 注入，此處只調整樣式) ── */
  section::after {
    font-family: 'Courier New', monospace;
    color: #585b70;
    font-size: 13px;
  }

  footer {
    position: absolute !important;
    top: 10px !important;
    right: 22px !important;
    bottom: auto !important;
    left: auto !important;
    height: auto !important;
    width: auto !important;
    padding: 6px 16px !important;
    line-height: 1 !important;
    font-size: 15px !important;
    color: #89b4fa !important;
    background: rgba(24, 24, 37, 0.55) !important;
    backdrop-filter: blur(8px) !important;
    -webkit-backdrop-filter: blur(8px) !important;
    border-radius: 10px !important;
    border: 1px solid rgba(255, 255, 255, 0.08) !important;
    cursor: pointer !important;
    z-index: 5 !important;
    opacity: 0;
    transition: opacity 0.25s ease;
    pointer-events: auto !important;
  }
  footer:hover {
    opacity: 1 !important;
  }
  section:hover footer {
    opacity: 0.6;
  }
---

<script>
document.addEventListener('click',function(e){for(var t=e.target;t;t=t.parentElement)if(t.tagName==='FOOTER'){location.href='./index.html';return}})
</script>

<!-- _paginate: false -->

# AI與我的人生

## 批判思考與生涯抉擇 期末報告

<br>

**班級**　國立雲林科技大學　資訊管理系 AI 技優專班
**學號**　B11223203　｜　**學生**　林奕安

---

## 目錄

1. **第一章**　AI vs 人類 — 本質差異
2. **第二章**　AI 做不到的事
3. **第三章**　AI對於我們的影響和挑戰
4. **第四章**　AI 的未來發展
5. **第五章**　AI 的倫理原則及創作者的版權問題
6. **學期總結**　學習心得與反思
7. **文獻依據**　參考資料

<img class="char-toc-r" src="./assets/character.png">

---

## 第一章 AI vs 人類 - 本質差異

我覺得其實目前所有的AI都只是傳統演算法及統計學的進化
之所以大家稱他是AI是因爲他給我們的output足夠讓我們驚豔

- 智慧的錯覺：是魔法還是統計學？
  - AI 的本質其實並非玄學，而是傳統演算法與機率統計的極致展現
  - 我們之所以感到驚豔，是因為算力與海量數據堆疊出的結果，超越了人類的直覺預測

- 本質差異：動態生長 vs 靜態模擬
  - 人類大腦（動態拓撲）： 神經元具備極高的**可塑性**，能隨時動態重建連結並規劃新路徑，單一模塊能處理極度高密度的複雜資訊
  - 人工智慧（靜態固化）： 在矽基晶片上以數學模型模擬神經元。一旦「訓練階段」結束，網路結構與權重就此凍結，無法像人類一樣在日常運作中持續進化。

---

## 第一章 AI vs 人類 - 本質差異

| 比較維度 (Aspect) | 人工智慧 (AI Intelligence) | 人類智慧 (Intelligence Human) |
| :--- | :--- | :--- |
| **學習 (Learning)** | 速度快，需要資料與演算法 | 速度慢，需要經驗與理解 |
| **創造力 (Creativity)** | 受限，基於模式與資料 | 高，能跳脫框架思考並創造新想法 |
| **情感 (Emotion)** | 缺乏情感與同理心 | 強大的情緒智商、同理心與社交技巧 |
| **記憶 (Memory)** | 能儲存海量資料並完美回憶 | 記憶容量有限，會隨時間遺忘 |
| **問題解決 (Problem Solving)** | 在特定任務上效率高，依賴預設邏輯 | 具備靈活、適應性強且直覺的問題解決能力 |
| **處理速度 (Processing Speed)** | 極快，能瞬間處理大型資料集 | 處理速度較慢，受認知負載與疲勞影響 |
| **適應性 (Adaptability)** | 需要重新訓練或重新編程才能適應 | 在動態環境中具備高度適應性 |
| **偏見 (Bias)** | 可能從訓練資料中繼承偏見 | 容易產生個人偏見，但具備自我反省能力 |
| **意識 (Consciousness)** | 沒有自我意識或意識 | 具備自我意識，能進行內省與主觀思考 |
| **能耗效率 (Energy Efficiency)** | 需要龐大的運算資源 | 相對於處理複雜任務，具備極高的能耗效率 |

![資料來源：CBitss](https://www.cbitss.in/ai-vs-human-intelligence/)
<div class="text-right">下一頁爆雷注意www</div>

---

<!-- _class: no-fade -->

## 第一章 AI vs 人類 - 本質差異

### 案例探討：AI 在「模仿」情緒嗎？

- 表象的溫度
    AI 能給出極度擬真、甚至讓人感到溫暖的回應 就像《ATRI》中的亞托莉，展現出豐富的喜怒哀樂，讓我們產生「她有靈魂」的驚豔感(AI)
  
- 底層的真相
    當男主角發現亞托莉被消除情感前留下的筆記本時，發現裡面寫滿了「遇到什麼情況，應該展現什麼表情與反應」的思考模式紀錄

- 計算出來的靈魂
    AI 的情感不是「感受」出來的，而是「計算」出來的。那本筆記本，就像是 AI 的權重矩陣 (Weight Matrix) 與決策樹 (Decision Tree)。AI 只是精準地讀取環境參數（Input），然後從預先訓練好的龐大資料庫中，**輸出最符合人類期待的情緒反應（Output）**

<img class="char-r" src="./assets/character-atri.png">

---

<!-- _class: no-fade -->

## 第一章 AI vs 人類 - 本質差異

### 案例探討：AI 在「模仿」情緒嗎？

- 表象的溫度
    AI 能給出極度擬真、甚至讓人感到溫暖的回應 就像《ATRI》中的亞托莉，展現出豐富的喜怒哀樂，讓我們產生「她有靈魂」的驚豔感(AI)
  
- 底層的真相
    當男主角發現亞托莉被消除情感前留下的筆記本時，發現裡面寫滿了「遇到什麼情況，應該展現什麼表情與反應」的思考模式紀錄

- 計算出來的靈魂
    AI 的情感不是「感受」出來的，而是「計算」出來的。那本筆記本，就像是 AI 的權重矩陣 (Weight Matrix) 與決策樹 (Decision Tree)。AI 只是精準地讀取環境參數（Input），然後從預先訓練好的龐大資料庫中，**輸出最符合人類期待的情緒反應（Output）**

<img class="char-bg-r" src="./assets/atri_cover.jpg">

---

## 第二章 AI 做不到的事

### AI 看似很強，但它其實**不懂**

- AI 就像一個**很會背書的學生**
  - 能快速翻遍所有課本，把內容整合成一篇漂亮的報告
  - 但它**不知道**這些內容哪個是對的、哪個是錯的
  - 更不知道教授（人類）覺得什麼才算**有趣、有新意**

<img class="char-deco" src="./assets/arona-sticker-3.png">
<div class="next-arrow">⌄</div>

---

## 第二章 AI 做不到的事

### 舉例：幫你寫論文？

| AI 能 | AI 不能 |
| :--- | :--- |
| 快速找 100 篇文獻並總結 | 告訴你這題目「會不會太老套」 |
| 生出漂亮的統計圖表 | 判斷這個地區的資料這樣分析**合不合理** |
| 模仿專家的語氣寫文章 | 感受這個主題在**當前社會敏感不敏感** |

---

## 第二章 AI 做不到的事

### AI 的創造力是假象

- 舉例：叫 AI 想一個新的商業點子
  - AI 會說：「結合 AI 與大數據，顛覆傳統產業」
  - 聽起來很對，但這是**已經存在**的排列組合
- 真正的創造，是像**賈伯斯做出 iPhone** — 沒有人這樣想過
- AI 無法跳脫既有框架，因為它的世界 = 它學過的資料

---

## 第二章 AI 做不到的事

### 有些「常識」課本沒寫

- 例：你問 AI 「這個研究題目可以嗎？」
  - AI 會說：「從文獻來看很合理」
  - 但它不知道：
    - 這個領域的大老**不喜歡**這種寫法
    - 這個主題最近**太敏感**，容易被罵
    - 某個審稿人**偏愛**哪種論述風格
- 這些「潛規則」只能靠**真正混過那個圈子**才知道

---

## 第二章 AI 做不到的事

### 小結：什麼是 AI 真正做不到的？

1. **理解** — 它處理文字，但不「懂」文字
2. **判斷** — 它不知道什麼重要、什麼可信
3. **創造** — 它只會重組，不會無中生有
4. **潛規則** — 它讀不到學術圈的「人情世故」

> AI 是很強的工具，但不是專家。**最終的判断還是需要人。**

---

## 第二章 AI 做不到的事

### 參考論文

> **Vibe Researching as Wolf Coming: Can AI Agents with Skills Replace or Augment Social Scientists?**  
> arXiv, 2026  
> 探討 AI 代理在社會科學研究中能做什麼、不能做什麼，以及顯性知識與隱性知識的關鍵差異

---

## 第三章 AI 對我們的影響和挑戰

### 工作：AI 會取代我們嗎？

- **不會完全取代，但會重新定義工作**
- 重複性高的工作（客服、翻譯、資料輸入）→ **大幅減少**
- 需要判斷、創意、人情味的工作 → **反而更珍貴**
- 未來不是「人 vs AI」，而是 **「會用 AI 的人 vs 不會用 AI 的人」**

<img class="char-deco" src="./assets/arona-sticker-1.png">
<div class="next-arrow">⌄</div>

---

## 第三章 AI 對我們的影響和挑戰

### 教育：考試還有意義嗎？

- AI 能輕鬆通過考試（律師、醫師、程式檢定）
- 那我們還學什麼？
  - 學**問對的問題**，而不是背答案
  - 學**批判思考**，而不是接受 AI 給的一切
  - 學**跨領域連結**，這才是 AI 最弱的地方

> 當 AI 能給答案，**會提問的人才是贏家。**

---

## 第三章 AI 對我們的影響和挑戰

### 資訊：真假難分

- AI 可以**完美偽裝**成人類寫文章、留言、造圖
- 帶來的問題：
  - **假新聞**更難辨識
  - **Deepfake** 讓影片也不能相信
  - **資訊焦慮** — 什麼是真的？
- 我們需要新的技能：**媒體識讀能力 2.0**

---

## 第三章 AI 對我們的影響和挑戰

### 心理：我們準備好了嗎？

- AI 越來越「像人」，我們會不會**過度依賴**？
  - 孤獨的人跟 AI 聊天 → 更不願意跟真人交流
  - 什麼都問 AI → 自己的思考能力退化
- **科技進步很快，但人類的心理適應沒那麼快**

---

## 第四章 AI 的未來發展

### 接下來會發生什麼？

| 短期（1-5 年） | 中期（5-15 年） | 長期（15 年+） |
| :--- | :--- | :--- |
| AI 融入日常工具（Office、Photoshop 都已內建） | AI 代理幫你處理複雜任務（訂機票、談判、寫合約） | 可能出現 **AGI**（通用人工智慧） |
| 多模態（文字+圖+聲音+影片）整合 | AI 參與科學研究（設計實驗、分析數據） | 人機共生？還是 AI 自主？ |

<img class="char-deco" src="./assets/arona-sticker-5.png">
<div class="next-arrow">⌄</div>

---

## 第四章 AI 的未來發展

### AGI 是什麼？離我們多遠？

- **AGI（通用人工智慧）**：像人類一樣，能處理任何智力任務
- 現在的 AI（ChatGPT 等）只是**狹義 AI** — 只會特定任務
- 專家意見分歧：
  - 樂觀派：2040 年前會實現
  - 保守派：可能永遠不會實現
- 關鍵瓶頸：AI 沒有**意識**、沒有**理解**、沒有**真正的自主學習**

---

## 第四章 AI 的未來發展

### 我怎麼看？

- AI 不會突然「覺醒」，而是會**慢慢地滲透**我們的生活
- 與其擔心 AI 統治世界，不如擔心：
  - **少數人掌握超強 AI** → 權力更集中
  - **AI 取代判斷** → 人類越來越懶得思考
  - **AI 偏見** → 錯誤的決策被放大

> 未來的關鍵不是 AI 多厲害，而是 **人類怎麼用它。**

---

## 第五章 AI 的倫理原則

### AI 需要遵守什麼？

目前國際間普遍接受的 AI 倫理原則：

| 原則 | 白話解釋 |
| :--- | :--- |
| **透明性** | 我們該知道眼前的是人還是 AI |
| **公平性** | AI 不能歧視（性別、種族、背景） |
| **問責性** | AI 出錯了，誰負責？ |
| **隱私保護** | AI 不能隨便蒐集你的資料 |
| **可控性** | 人類要有能力關掉 AI |

---

## 第五章 AI 的倫理原則

### 透明性：你有權知道

- 你正在跟 AI 聊天，還是真人客服？
- 這張圖是 AI 畫的，還是藝術家畫的？
- 這篇文章是 AI 寫的，還是記者寫的？

→ **標示義務**：使用 AI 生成的內容應該**明確標註**

- 臺灣、歐盟都在推動 AI 生成內容的**強制標示法規**

---

## 第五章 創作者的版權問題

### AI 的訓練資料從哪來？

- AI 學了網路上的**海量資料**（文章、圖片、程式碼、音樂）
- 問題：**這些資料的作者同意了嗎？**
  - 新聞網站的文章 → 被拿去訓練 → 沒付錢
  - 插畫家的畫風 → 被 AI 模仿 → 沒授權
  - 程式碼 → 被 AI 學走 → 開源授權有被遵守嗎？

---

## 第五章 創作者的版權問題

### AI 生成的作品，版權算誰的？

- 目前各國法律還在打架：
  - **美國**：AI 生成的內容**不具版權**（因為不是人類創作的）
  - **歐盟**：正在討論，傾向要求**人類有「重大貢獻」**才算
  - **臺灣**：尚無明確規範
- 灰色地帶：
  - 你用 AI 生圖 → 稍微改一下 → 算你的嗎？
  - 你用 AI 寫 code → 整份專案的版權歸誰？

---

## 第五章 創作者的版權問題

### 舉例：真實發生的爭議

| 事件 | 問題 |
| :--- | :--- |
| Getty Images 告 Stability AI | AI 未經授權使用 1200 萬張圖庫照片訓練 |
| 《紐約時報》告 OpenAI | ChatGPT 直接輸出付費文章的內容 |
| 插畫家集體抗議 | AI 能模仿特定畫風，導致接案機會減少 |

> **結論**：科技跑在法律前面，版權制度正在被迫改革

---

## 學期總結　學習心得與反思

本學期學到了很多邏輯思考的方法。讓我驚喜的是，課堂上分析柯南推理結構的方式，跟我這學期同步修習的**離散數學**有高度相似之處：

- **「若 P 則 Q」**的條件關係 → 在柯南的破案邏輯中隨處可見
- **反證法** → 推翻嫌疑人不在場證明的常見手法
- **命題邏輯與推論規則** → 與老師講解的邏輯分析如出一轍

這種跨課程的共鳴，讓我感受到**邏輯思維的普遍性與重要性**——它不只是數學課的內容，而是解決問題的根本能力。

<img class="char-deco" src="./assets/arona-sticker-8.png">
<div class="next-arrow">⌄</div>

---

## 文獻依據　參考資料（1/2）

1. **AI vs Human Intelligence** — CBitss  
   <https://www.cbitss.in/ai-vs-human-intelligence/>

2. **Vibe Researching as Wolf Coming: Can AI Agents with Skills Replace or Augment Social Scientists?** — arXiv, 2026  
   <https://arxiv.org/abs/26oi>

3. **Noy, S. & Zhang, W. (2023).** Experimental evidence on the productivity effects of generative artificial intelligence. *Science*, 381(6654), 187-192.  
   <https://doi.org/10.1126/science.adh2586>

4. **Liang, W. et al. (2025).** Monitoring AI-Modified Content at Scale. *arXiv preprint*.  
   <https://arxiv.org/abs/2503.00oi>

---

## 文獻依據　參考資料（2/2）

5. **Evans, J.A. & Foster, J.G. (2011).** Metaknowledge. *Science*, 331(6018), 721-725.  
   <https://doi.org/10.1126/science.1201765>

6. **Granovetter, M.S. (1973).** The Strength of Weak Ties. *American Journal of Sociology*, 78(6), 1360-1380.  
   <https://doi.org/10.1086/225469>

7. **Tilly, C. (1998).** *Durable Inequality*. University of California Press.  
   <https://books.google.com/books?id=ouVqBgAAQBAJ>

8. **Collins, H. & Evans, R. (2007).** *Rethinking Expertise*. University of Chicago Press.  
   <https://doi.org/10.7208/chicago/9780226113624>

---

<!-- _class: thanks -->

# 謝謝各位

<img class="thanks-gif" src="./assets/Aris.gif">

---
