---
permalink: /slide/
title: "TA Session Slides"
author_profile: true
---

Here are the weekly TA session slides. Please Download before classes.


<style>
  /* 彈出視窗（Lightbox）的樣式設定 */
  .pdf-modal {
    border: none;
    border-radius: 8px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.3);
    width: 80%;
    max-width: 900px;
    height: 80vh;
    padding: 0;
  }
  .pdf-modal::backdrop {
    background: rgba(0, 0, 0, 0.6);
    backdrop-filter: blur(3px);
  }
  .modal-header {
    background: #003366;
    color: white;
    padding: 12px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-weight: bold;
  }
  .close-btn {
    background: none;
    border: none;
    color: white;
    font-size: 20px;
    cursor: pointer;
  }
  .preview-link {
    cursor: pointer;
    color: #003366;
    font-weight: bold;
    text-decoration: underline;
    margin-left: 10px;
  }
</style>

### Weekly Slides

<ul>
  <li>
    <b>Week 01：</b> R 環境安裝與基礎 
    <span class="preview-link" onclick="openPreview('{{ site.url }}/files/W1_Intro.pdf', 'Week 01 講義預覽')">👁️ 線上預覽</span> | 
    <a href="{{ site.url }}/files/W1_Intro.pdf">📥 下載</a>
  </li>
  <li style="margin-top: 10px;">
    <b>Week 02：</b> 敘述統計與 Tidyverse 
    <span class="preview-link" onclick="openPreview('{{ site.url }}/files/W2_Descriptive.pdf', 'Week 02 講義預覽')">👁️ 線上預覽</span> | 
    <a href="{{ site.url }}/files/W2_Descriptive.pdf">📥 下載</a>
  </li>
  <li style="margin-top: 10px;">
    <b>Week 03：</b> 機率分佈與繪圖 — <span style="color: #999;">尚未公佈</span>
  </li>
</ul>

<dialog id="pdfDialog" class="pdf-modal">
  <div class="modal-header">
    <span id="modalTitle">講義預覽</span>
    <button class="close-btn" onclick="closePreview()">&times;</button>
  </div>
  <iframe id="pdfFrame" src="" width="100%" height="calc(100% - 48px)" style="border: none;"></iframe>
</dialog>

<script>
  const dialog = document.getElementById('pdfDialog');
  const frame = document.getElementById('pdfFrame');
  const title = document.getElementById('modalTitle');

  function openPreview(pdfUrl, weekTitle) {
    title.innerText = weekTitle;
    frame.src = pdfUrl;
    dialog.showModal();
  }

  function closePreview() {
    dialog.close();
    frame.src = ""; // 關閉時清空，釋放記憶體並停止背景載入
  }

  // 點擊視窗外面（背景）也能自動關閉
  dialog.addEventListener('click', (e) => {
    if (e.target === dialog) {
      closePreview();
    }
  });
</script>