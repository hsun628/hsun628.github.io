---
permalink: /announcements/
title: "All Announcements"
author_profile: true
---

Check all previous announcements!

---

<style>
  /* 歷史公告外框：維持不顯眼的細灰框，並改為 10px 圓角 */
  .announcement-box {
    border: 1px solid #e2e8f0;
    padding: 18px 20px;
    border-radius: 10px;
    background-color: #ffffff;
    margin-bottom: 12px;
  }
  
  /* 移除 HTML5 預設的箭頭圖標，並設定橫向排列 */
  .announcement-box summary {
    list-style: none;
    outline: none;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .announcement-box summary::-webkit-details-marker {
    display: none;
  }
  
  /* 標題樣式：拔掉強制的顏色限制，讓原生 H4 自動對齊主題標題色 */
  .announcement-title {
    margin: 0;
  }
  
  /* 預設隱藏完整內容 */
  .announcement-content {
    display: none;
    margin-top: 15px;
    border-top: 1px dashed #e2e8f0;
    padding-top: 15px;
    line-height: 1.65;
    font-size: 0.95em;
  }
  
  /* 展開狀態：顯示完整內容 */
  .announcement-box[open] .announcement-content {
    display: block;
  }
  
  /* 展開狀態：隱藏 [more ↓] 按鈕 */
  .announcement-box[open] .more-btn {
    display: none;
  }
  
  /* [more ↓] 按鈕樣式：微調回呼應主題大標題的灰色調 */
  .more-btn {
    color: #003366;
    font-size: 0.85em;
    font-weight: bold;
    text-decoration: underline;
    white-space: nowrap;
    margin-left: 15px;
  }

  /* ======================================================== */
  /* 深色模式自適應                                            */
  /* ======================================================== */
  @media (prefers-color-scheme: dark) {
    .announcement-box {
      background-color: #252a34;
      border-color: #3f444e;
    }
    .more-btn {
      color: inherit;
      opacity: 0.8;
    }
  }
  
  html[data-theme="dark"] .announcement-box,
  .theme-dark .announcement-box {
    background-color: #252a34;
    border-color: #3f444e;
  }
  
  html[data-theme="dark"] .more-btn,
  .theme-dark .more-btn {
    color: inherit;
    opacity: 0.8;
  }
</style>

<!-- 新公告 -->
<details class="announcement-box">
  <summary>
    <h4 class="announcement-title">2026-06-13: Welcome to the course!</h4>
    <span class="more-btn">more &darr;</span>
  </summary>
  <div class="announcement-content">
    Welcome to the Statistics TA session! The website is now fully set up. You can explore and download weekly handouts, sample codes, and other course materials using the menu at the top right of this page. Feel free to contact me if you have any question or suggestion about the website!
  </div>
</details>

<!-- 舊公告（未來新增公告時，只要複製上方 details 區塊即可） -->