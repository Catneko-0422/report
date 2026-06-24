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

  section > * { position: relative; z-index: 1; }

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

  section.no-fade > * {
    animation: none !important;
  }

  section > *:nth-child(2) { animation-delay: 0.06s; }
  section > *:nth-child(3) { animation-delay: 0.12s; }
  section > *:nth-child(4) { animation-delay: 0.18s; }
  section > *:nth-child(5) { animation-delay: 0.24s; }
  section > *:nth-child(6) { animation-delay: 0.30s; }
  section > *:nth-child(7) { animation-delay: 0.36s; }

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

  strong {
    color: #cba6f7;
    font-weight: 600;
  }

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

  code {
    background: rgba(243, 139, 168, 0.18);
    color: #f38ba8;
    padding: 3px 10px;
    border-radius: 8px;
    font-size: 0.86em;
    font-weight: 500;
    letter-spacing: 0.01em;
  }

  .char-r, .char-l, .char-toc-r {
    position: absolute;
    z-index: 2;
  }

  .char-toc-r {
    top: 50%;
    transform: translateY(-50%);
    height: 100%;
    right: -0px;
  }

  .char-r {
    top: 80%;
    transform: rotate(-10deg) translateY(-50%);
    height: 150%;
    right: -380px;
  }

  .char-l {
    left: 40px;
  }

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

  section:has(.char-r, .char-bg-r, .char-toc-r) {
    padding-right: 450px;
  }
  section:has(.char-l, .char-bg-l) {
    padding-left: 450px;
  }

  .text-right { text-align: right !important; }

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

# ERP 生管料號自動編碼輔助系統

## CSIE 2188 · 自然語言處理導論 · 期末專題進度報告

<br>

**組長**　林奕安　B11223203　｜　**組員**　黃玄燁　B11223224
**指導教師**　Michael Lee

<img class="char-deco" src="./assets/arona-sticker-5.png">

---

## 報告大綱

1. **01**　研究背景與動機
2. **02**　研究方法
3. **03**　研究分工
4. **04**　甘特圖
5. **05**　目前進度
6. **06**　初步成果 Demo
7. **07**　結論與下一步

<img class="char-toc-r" src="./assets/character.png">

---

## 01　研究背景與動機

### 問題描述

電子企業導入 ERP 系統時，每個料件（電子零件、PCB、電容器等）須由生管產生一組唯一且具規則性的 **16 碼料號（PART NO.）**。

目前多數企業仍依賴人工查表編碼，存在以下問題：

- **失誤率高** — 不同操作員對同一規格可能給出不同編碼
- **時間成本高** — 查閱編碼規則，每筆料號需耗時數分鐘
- **員工訓練成本高** — 新人需進行培訓以熟悉編碼規則
- **稽核風險** — 無法追溯料號的產生時間、人員與規則版本

---

## 01　研究背景與動機

### 研究動機

我們希望開發一套自動化系統，並引入 **LLM** 來解決問題：

- **RAG** — 檢索編碼規則文件
- **Finetune** — 使用人工標註的現成資料進行微調

預期效益：

| 面向 | 效益 |
| :--- | :--- |
| **正確性** | 降低失誤率，提升料號一致性 |
| **效率** | 減少時間成本，操作簡單降低訓練成本 |
| **可追溯性** | 可管理編碼原則的不同版本，追溯料號生產過程 |

<img class="char-deco" src="./assets/arona-sticker-3.png">

---

## 02　研究方法

### 技術路線

| 步驟 | 內容 |
| :--- | :--- |
| **Step 1** | 資料收集 & 前處理 |
| **Step 2** | 模型架構選擇 |
| **Step 3** | 訓練 / 微調 |
| **Step 4** | 評估 & 實驗 |

### 使用技術 / 框架

- **後端** — Flask 3 + Python 3.14（UV 管理版本）
- **前端** — React 19 + TypeScript + Vite 8
- **資料庫** — PostgreSQL 16 + Redis 7
- **RAG 管道** — LangChain + 向量檢索
- **容器化** — Docker Compose
- **認證機制** — JWT + Argon2 + RBAC

---

## 02　研究方法

### 模型選擇

`llama-3.1-8b-instant`

- 極低延遲
- 支援工具呼叫與結構化輸出
- 適合查詢資料庫及產生固定格式資料（生產編碼）
- 可於本地端自行部署，符合企業資料保護需求

### 資料集 & 評估指標

- **資料集來源** — 企業提供資料
- **評估指標** — Accuracy、Recall

---

## 02　研究方法

### 系統架構圖

```mermaid
flowchart TB
    subgraph Client["前端 (React 19 + Vite 8)"]
        CP["CodingPage<br/>點選編碼 + AI 自動填充"]
        RTE["RuleTreeEditor<br/>規則樹編輯器"]
    end

    subgraph Backend["後端 (Flask + Gunicorn)"]
        API["API Blueprints<br/>auth / admin / rule_tree<br/>encode / auto_encode"]
        LS["LLM Service<br/>LangChain + ChatOllama<br/>+ ReAct Agent"]
        MCP["MCP Tools<br/>get_material_rules<br/>query_rag_examples<br/>extract_field_patterns"]
    end

    subgraph DB["資料庫"]
        PG[("PostgreSQL 16<br/>users / rule_tree_nodes(2654)<br/>part_numbers(363) / audit_logs")]
        RD[("Redis 7<br/>規則樹快取 5min<br/>Rate Limiting")]
    end

    subgraph AI["AI 推論"]
        OL["Ollama"]
        GM["Gemma4:latest<br/>Q4_K_M · temp=0"]
        OL --- GM
    end

    Client -->|HTTP / SSE| API
    API --> LS
    LS --> MCP
    MCP -.->|查詢| DB
    LS -->|ChatOllama| OL
    API --> PG
    API --> RD

    classDef client fill:#fce4ec,stroke:#880e4f
    classDef backend fill:#e1f5fe,stroke:#01579b
    classDef db fill:#e8f5e9,stroke:#1b5e20
    classDef ai fill:#f3e5f5,stroke:#4a148c
    class CP,RTE client
    class API,LS,MCP backend
    class PG,RD db
    class OL,GM ai
```

---

## 02　研究方法

### LLM 自動編碼流程 (ReAct Agent)

```mermaid
flowchart LR
    START(["使用者填寫規格<br/>Description / MFG Part / Vendor PN"]) --> PROMPT

    subgraph PROMPT["① 組裝 Rich Prompt（全部 inline）"]
        PI["━━ PRODUCT INFO ━━<br/>Description: CHIP RESISTOR...<br/>MFG Part: RC0603FR-0710KL"]
        FI["Encoding Fields:<br/>Field 0: 電阻種類 [01]貼片 [02]碳膜<br/>Field 1: 電阻值 (input, 4 chars)"]
        HI["History:<br/>1001R-002 → 電容值=10U0"]
    end

    PROMPT --> AGENT

    AGENT["② ReAct Agent<br/>create_react_agent"] --> TOOL{"③ 可選用 MCP 工具"}
    TOOL --> RULES["get_material_rules<br/>查詢編碼規則樹"]
    TOOL --> RAG["query_rag_examples<br/>搜尋歷史料號(RAG)"]
    TOOL --> PATTERN["extract_field_patterns<br/>分析編碼模式"]

    RULES & RAG & PATTERN --> AGENT
    AGENT --> LLM["④ Gemma4 推論<br/>temperature=0<br/>num_predict=8192"]
    LLM --> PARSE["⑤ JSON 解析<br/>_extract_json()"]
    PARSE --> MATCH["⑥ 四層模糊匹配<br/>exact code → label → regex → difflib"]
    MATCH --> RESULT["⑦ 回傳結果<br/>field_predictions (node_id)<br/>+ field_confidences (0.0~1.0)"]
```

---

## 03　研究分工

| 角色 | 姓名 | 學號 | 負責工作 | 進度 |
| :--- | :--- | :--- | :--- | :---: |
| **組長** | 林奕安 | B11223203 | 資料蒐集、前後端整合、模型架構設計、模型訓練與優化 | 100% |
| **組員** | 黃玄燁 | B11223224 | 資料清洗、資料庫架設、簡報撰寫、上台報告 | 100% |

<img class="char-deco" src="./assets/arona-sticker-1.png">

---

## 04　甘特圖 — 時程規劃

| 工作項目 | W10 | W11 | W12 | W13 | W14 | W15 | W16 | W17 |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 題目確認 & 文獻 | ✓ | ✓ | | | | | | |
| 資料收集 & 清洗 | | ✓ | ✓ | | | | | |
| 系統架構設計 | | | ✓ | ✓ | | | | |
| 模型訓練 / 微調 | | | | ✓ | ✓ | ✓ | | |
| 介面 & Demo 建置 | | | | | ✓ | ✓ | | |
| 評估與測試 | | | | | | ✓ | ✓ | |
| 報告撰寫 | | | | | | | ✓ | ✓ |
| 期末發表 | | | | | | | | ✓ |

---

## 05　目前進度

### 整體完成度 — 100%

| 狀態 | 項目 |
| :--- | :--- |
| **已完成** | 題目確認與小組分工、完整前後端系統架構設計與實作、資料庫設計（users, roles, audit_logs, rule_tree_categories, rule_tree_nodes, part_numbers） |
| **已完成** | RBAC 角色權限控管（Admin / RuleMaker / User）、認證系統（註冊、審核、登入、JWT、改密碼） |
| **已完成** | 規則樹編輯器（CRUD、折疊 / 展開、樂觀更新、內聯新增、排序）、Docker Compose 一鍵部署 |
| **已完成** | LLM / Ollama API 整合與 RAG 管道建置、編碼資料取得並 Finetune、Prompt engineering |
| **已完成** | 端到端 LLM 自動編碼流程整合、完整評估實驗（準確率、召回率）、效能最佳化 |
| **已完成** | 期末報告撰寫與發表準備 |

<div class="next-arrow">⌄</div>

---

## 06　初步成果 Demo

### 功能亮點

- **RBAC 權限管理** — 不同角色有不同的權限，以利管理編碼規則與生產編碼
- **規則樹編輯器** — 可新增編碼規則，以應對各式不同環境
- **LLM 自動編碼** — LLM 依照 RAG 管道學習編碼規則，按照規則生成符合使用者需求的生產編碼
- **高準確率** — 根據 LLM 生成出來的編碼，其正確率達到 **99%**，大幅減少人工失誤率與時間成本

> *系統截圖與展示影片請在報告時播放*

---

## 07　結論與下一步

### 主要發現

- 透過 LLM 模型快速生產出大量不同料號，大幅減少生管編碼的時間成本

### 技術亮點

- 可依照不同環境下設計規則樹，使編碼規則對於環境變遷具有一定彈性

### 下一步計畫

- 使企業引入該項技術，並獲得更多使用回饋

---

## 07　結論與下一步

### 遇到的困難

- 某些特定料號規則的資料不夠充足，導致準確率下降
  - → 人工標註新增更多訓練資料，屢次確認編碼結果是否符合編碼規則

### 學習心得

> **林奕安**：用寒假的打工經驗來做這個 ERP 專案，串接 LLM、RAG、規則樹和 BOM 匯入，深刻體會到資料品質與 Prompt 設計對 AI 準確度的關鍵影響。

> **黃玄燁**：透過本次專題，我學習到 LLM 與 RAG 的重要性，並加以實際應用於企業需求上。學習到了自然語言處理在企業實務中的應用價值，獲益良多。

---

<!-- _class: thanks -->

# 感謝聆聽　歡迎提問

<p>CSIE 2188 · 自然語言處理導論 · 指導教師：Michael Lee · 2026-06</p>

<img class="thanks-gif" src="./assets/Aris.gif">
