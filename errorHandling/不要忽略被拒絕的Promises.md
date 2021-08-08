---
layout: two-cols
---

<template v-slot:default>

# <h3 class="awful">❌ 糟糕的</h3>
```ts
getdata()
  .then(data => {
    functionThatMightThrow(data);
  })
  .catch(error => {
    console.log(error);
  });
```

</template>

<template v-slot:right>

# <h3 class="adequate">✅ 適當的</h3>

```ts
// 不要忽略被拒絕的 Promises
getdata()
  .then(data => {
    functionThatMightThrow(data);
  })
  .catch(error => {
    // 可以這樣（會比 console.log 更吵）
    console.error(error);
    // 或這種方法
    notifyUserOfError(error);
    // 另外一種方法
    reportErrorToService(error);
    // 或是全部都做！
  });
```

</template>
