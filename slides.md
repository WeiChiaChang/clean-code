---
# try also 'default' to start simple
theme: bricks
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: true
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# Fonts
---

<h1 class="title">Clean Code</h1>

<p class="subtitle">In JavaScript</p>

---

# 目錄

- **變數** - Variables
- **函數** - Functions
- **物件與資料結構** - Objects & Data Structure
- **類別** - Classes
- **物件導向基本原則** - SOLID
- **測試** - Testing
- **並發** - Concurrency
- **錯誤處理** - Error Handling
- **格式化** - Formatting
- **註解** - Comments

<style>
h1 {
  color: #4EC5D4;
}
</style>

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>變數</h1>
    <p>Variables</p>
  </div>
</div>

---
src: ./variables/使用具有意義且可閱讀的名稱.md
---

---
src: ./variables/相同類型的變數使用相同的名稱.md
---

---
src: ./variables/使用可搜尋的名稱.md
---

---
src: ./variables/使用可解釋的變數.md
---

---
src: ./variables/避免心理作用1.md
---

---
src: ./variables/避免心理作用2.md
---

---
src: ./variables/避免使用不必要的描述1.md
---

---
src: ./variables/避免使用不必要的描述2.md
---

---
src: ./variables/使用預設參數代替條件判斷.md
---

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>函數</h1>
    <p>Functions</p>
  </div>
</div>

---
src: ./functions/參數1.md
---

---
src: ./functions/參數2.md
---

---
src: ./functions/參數3.md
---

---
src: ./functions/一個函數只做一件事情.md
---

---
src: ./functions/函數名稱應該說明它做的內容.md
---

---
src: ./functions/移除重複的程式碼1.md
---

---
src: ./functions/移除重複的程式碼2.md
---

---
src: ./functions/移除重複的程式碼3.md
---

---
src: ./functions/設定Objects的預設值1.md
---

---
src: ./functions/設定Objects的預設值2.md
---

---
src: ./functions/不要使用旗標作為參數.md
---

---
src: ./functions/避免副作用.md
---

---
src: ./functions/避免副作用之二.md
---

---
src: ./functions/避免全域函數.md
---

---
src: ./functions/使用函數式設計代替命令式程式設計1.md
---

---
src: ./functions/使用函數式設計代替命令式程式設計2.md
---

---
src: ./functions/避免負面狀態.md
---

---
src: ./functions/避免型別檢查.md
---

---
src: ./functions/避免型別檢查之二1.md
---

---
src: ./functions/避免型別檢查之二2.md
---

---
src: ./functions/別過度優化.md
---

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>物件與資料結構</h1>
    <p>Objects & Data Structure</p>
  </div>
</div>

---
src: ./functions/使用getters與setters1.md
---

---
src: ./functions/使用getters與setters2.md
---

---
src: ./functions/讓物件擁有私有成員1.md
---

---
src: ./functions/讓物件擁有私有成員2.md
---

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>類別</h1>
    <p>Classes</p>
  </div>
</div>

---
src: ./classes/類別語法偏好使用ES6.md
---

---
src: ./classes/使用方法鏈1.md
---

---
src: ./classes/使用方法鏈2.md
---

---
src: ./classes/偏好組合更甚於繼承1.md
---

---
src: ./classes/偏好組合更甚於繼承2.md
---

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>物件導向基本原則</h1>
    <p>SOLID</p>
  </div>
</div>

---
src: ./SOLID/單一功能原則1.md
---

---
src: ./SOLID/單一功能原則2.md
---

---
src: ./SOLID/開閉原則1.md
---

---
src: ./SOLID/開閉原則2.md
---

---
src: ./SOLID/裡氏替換原則1.md
---

---
src: ./SOLID/裡氏替換原則2.md
---

---
src: ./SOLID/介面隔離原則1.md
---

---
src: ./SOLID/介面隔離原則2.md
---

---
src: ./SOLID/依賴反轉原則1.md
---

---
src: ./SOLID/依賴反轉原則2.md
---

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>測試</h1>
    <p>Testing</p>
  </div>
</div>

---
src: ./testing/每個測試只測試一個概念1.md
---

---
src: ./testing/每個測試只測試一個概念2.md
---

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>並發</h1>
    <p>Concurrency</p>
  </div>
</div>

---
src: ./concurrency/async.md
---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>錯誤處理</h1>
    <p>Error Handling</p>
  </div>
</div>

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>格式化</h1>
    <p>Formatting</p>
  </div>
</div>

---

<div class="slidev-layout cover text-center">
  <div class="my-auto w-full">
    <h1>註解</h1>
    <p>Comments</p>
  </div>
</div>
