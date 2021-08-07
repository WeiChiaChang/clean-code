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

# 變數

使用有意義且具備可讀性的名稱

<h3 class="awful">❌ 糟糕的</h3>

```javascript
const yyyymmdstr = moment().format('YYYY/MM/DD');
```

<v-click>
  <h3 class="adequate">✅ 適當的</h3>

  ```javascript
  const currentDate = moment().format('YYYY/MM/DD');
  ```
</v-click>

---

# 變數

相同類型的變數使用相同的名稱

<h3 class="awful">❌ 糟糕的</h3>

```javascript
getUserInfo();
getClientData();
getCustomerRecord();
```

<v-click>
  <h3 class="adequate">✅ 適當的</h3>

  ```javascript
  getUser();
  ```
</v-click>

---

# 變數

使用可搜尋的名稱

<h3 class="awful">❌ 糟糕的</h3>

```javascript
// 86400000 代表什麼意義？
setTimeout(blastOff, 86400000);
```

<v-click>
  <h3 class="adequate">✅ 適當的</h3>

  ```javascript
  // 宣告（Declare）一個有意義的常數（constants）
  const MILLISECONDS_IN_A_DAY = 86400000;

  setTimeout(blastOff, MILLISECONDS_IN_A_DAY);
  ```
</v-click>

---

# 變數

使用可解釋的變數

<h3 class="awful">❌ 糟糕的</h3>

```javascript
const address = 'One Infinite Loop, Cupertino 95014';
const cityZipCodeRegex = /^[^,\\]+[,\\\s]+(.+?)\s*(\d{5})?$/;
saveCityZipCode(
  address.match(cityZipCodeRegex)[1],
  address.match(cityZipCodeRegex)[2]
);
```

<v-click>
  <h3 class="adequate">✅ 適當的</h3>

```ts {3}
const address = 'One Infinite Loop, Cupertino 95014';
const cityZipCodeRegex = /^[^,\\]+[,\\\s]+(.+?)\s*(\d{5})?$/;
const [, city, zipCode] = address.match(cityZipCodeRegex) || [];
saveCityZipCode(city, zipCode);
```
</v-click>

---

# 變數

避免心理作用（Mental Mapping）

<h3 class="awful">❌ 糟糕的</h3>

```javascript
const locations = ['Austin', 'New York', 'San Francisco'];
locations.forEach(l => {
  doStuff();
  doSomeOtherStuff();
  // ...
  // ...
  // ...
  // 等等，這 `l` 是…？
  dispatch(l);
});
```

---

# 變數

避免心理作用（Mental Mapping）

<h3 class="adequate">✅ 適當的</h3>

```javascript
const locations = ['Austin', 'New York', 'San Francisco'];
locations.forEach(location => {
  doStuff();
  doSomeOtherStuff();
  // ...
  // ...
  // ...
  dispatch(location);
});
```
---

# 變數

避免使用不必要的描述（Context）

<h3 class="awful">❌ 糟糕的</h3>

```javascript
const Car = {
  carMake: 'Honda',
  carModel: 'Accord',
  carColor: 'Blue'
};

function paintCar(car) {
  car.carColor = 'Red';
}
```
---

# 變數

避免使用不必要的描述（Context）

<h3 class="adequate">✅ 適當的</h3>

```javascript
const Car = {
  make: 'Honda',
  model: 'Accord',
  color: 'Blue'
};

function paintCar(car) {
  car.color = 'Red';
}
```
---

# 變數

使用預設參數代替條件判斷

<h3 class="awful">❌ 糟糕的</h3>

```javascript
function createMicrobrewery(name) {
  const breweryName = name || 'Hipster Brew Co.';
  // ...
}
```

<v-click>
  <h3 class="adequate">✅ 適當的</h3>

  ```javascript
  function createMicrobrewery(name = 'Hipster Brew Co.') {
    // ...
  }
  ```
</v-click>

---
layout: two-cols
---

<template v-slot:default>

# <h3 class="awful">❌ 糟糕的</h3>

```ts {2-3|5|all}
function add(
  a: Ref<number> | number,
  b: Ref<number> | number
) {
  return computed(() => unref(a) + unref(b))
}
```

</template>
<template v-slot:right>

# <h3 class="adequate">✅ 適當的</h3>

This shows on the right

</template>