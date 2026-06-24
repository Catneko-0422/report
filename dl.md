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

# 深度學習

## 期末報告

<br>

**班級**　國立雲林科技大學　資訊管理系 AI 技優專班
**學號**　B11223203　｜　**學生**　林奕安

---

## 目錄

1. **第一章**　神經網路基礎
2. **第二章**　卷積神經網路
3. **第三章**　循環神經網路
4. **第四章**　生成對抗網路
5. **第五章**　強化學習
6. **第六章**　應用與展望
7. **學期總結**　學習心得與反思
8. **文獻依據**　參考資料

<img class="char-toc-r" src="./assets/character.png">

---

## 第一章　神經網路基礎

- 感知機與多層感知機
  - 線性分類 → 非線性活化函數
  - Sigmoid、ReLU、Tanh

- 反向傳播演算法
  - 鏈鎖法則與梯度下降
  - 學習率與優化器（SGD、Adam）

---

## 第二章　卷積神經網路

- 卷積運算
  - 濾波器（Kernel）與特徵圖
  - 池化層（Pooling）

- 經典架構
  - LeNet-5、AlexNet、VGGNet
  - ResNet 與殘差連接

---

## 第三章　循環神經網路

- 序列建模
  - RNN 的梯度消失與爆炸問題
  - LSTM 的遺忘閘、輸入閘、輸出閘

- 應用場景
  - 語音辨識
  - 時間序列預測

---

## 第四章　生成對抗網路

- 對抗式訓練
  - 生成器（Generator） vs 鑑別器（Discriminator）
  - 納許均衡與訓練穩定性

- 經典變體
  - DCGAN、CycleGAN、StyleGAN
  - 擴散模型（Diffusion Models）

---

## 第五章　強化學習

- 馬可夫決策過程
  - 狀態、動作、獎勵
  - 策略與價值函數

- Deep RL
  - DQN（深度 Q 網路）
  - Policy Gradient、Actor-Critic

---

## 第六章　應用與展望

| 領域 | 應用 |
| :--- | :--- |
| **電腦視覺** | 影像分類、物件偵測、語意分割 |
| **自然語言** | 機器翻譯、情感分析、對話系統 |
| **醫療** | 醫學影像診斷、藥物發現 |
| **自動駕駛** | 感知、決策、控制 |

---

## 學期總結　學習心得與反思

從 MLP 到 Transformer、擴散模型，深度學習的演進速度令人驚嘆。

- 掌握基礎理論（反向傳播、梯度下降）是理解一切的前提
- 硬體進步（GPU、TPU）大幅推動了模型規模的擴張
- 未來關鍵：**可解釋性、資料效率、能源效率**

深度學習不是萬能藥，但作為一個強大的工具，值得持續投入學習。

<img class="char-deco" src="./assets/arona-sticker-3.png">
<div class="next-arrow">⌄</div>

---

## 文獻依據　參考資料

1. **Goodfellow, I., Bengio, Y. & Courville, A. (2016).** *Deep Learning*. MIT Press.  
   <https://www.deeplearningbook.org/>

2. **Krizhevsky, A., Sutskever, I. & Hinton, G.E. (2012).** ImageNet Classification with Deep Convolutional Neural Networks. *NeurIPS*.

3. **He, K. et al. (2016).** Deep Residual Learning for Image Recognition. *CVPR*.  
   <https://arxiv.org/abs/1512.03385>

4. **Goodfellow, I. et al. (2014).** Generative Adversarial Nets. *NeurIPS*.

5. **Mnih, V. et al. (2015).** Human-level control through deep reinforcement learning. *Nature*, 518(7540), 529-533.

---

<!-- _class: thanks -->

# 謝謝各位

<img class="thanks-gif" src="./assets/Aris.gif">
