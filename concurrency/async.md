---
layout: two-cols
---

<template v-slot:default>

# <h3 class="awful">❌ 糟糕的</h3>

```ts
import { get } from 'request-promise';
import { writeFile } from 'fs-promise';

get('https://en.wikipedia.org/wiki/Robert_Cecil_Martin')
  .then(response => {
    return writeFile('article.html', response);
  })
  .then(() => {
    console.log('File written');
  })
  .catch(err => {
    console.error(err);
  });
```

</template>

<template v-slot:right>

# <h3 class="adequate">✅ 適當的</h3>

```ts
// Async/Await 比 Promises 更加簡潔
import { get } from 'request-promise';
import { writeFile } from 'fs-promise';

async function getCleanCodeArticle() {
  try {
    const response = await get(
      'https://en.wikipedia.org/wiki/Robert_Cecil_Martin'
    );
    await writeFile('article.html', response);
    console.log('File written');
  } catch (err) {
    console.error(err);
  }
}
```

</template>
