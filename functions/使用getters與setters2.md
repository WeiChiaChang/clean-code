---
layout: two-cols
---

<template v-slot:default>

# <h3 class="awful">❌ 糟糕的</h3>

```ts
function makeBankAccount() {
  // ...
  return {
    balance: 0
    // ...
  };
}

const account = makeBankAccount();
account.balance = 100;
```

</template>

<template v-slot:right>

# <h3 class="adequate">✅ 適當的</h3>

```ts
function makeBankAccount() {
  // 私有變數
  let balance = 0;
  // 'getter'，經由下方的返回物件對外公開
  function getBalance() {
    return balance;
  }
  // 'setter'，經由下方的返回物件對外公開
  function setBalance(amount) {
    // ... 更新前先進行驗證
    balance = amount;
  }

  return {
    // ...
    getBalance,
    setBalance
  };
}

const account = makeBankAccount();
account.setBalance(100);
```

</template>
