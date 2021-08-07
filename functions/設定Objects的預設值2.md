# 使用 Object.assign 做預設值

<h3 class="adequate">✅ 適當的</h3>

```ts
const menuConfig = {
  title: 'Order',
  // 漏掉 body
  buttonText: 'Send',
  cancellable: true
};
function createMenu(config) {
  config = Object.assign(
    {
      title: 'Foo',
      body: 'Bar',
      buttonText: 'Baz',
      cancellable: true
    },
    config
  );
  // config 現在等同於： { title: 'Order', body: 'Bar', buttonText: 'Send', cancellable: true }
}

createMenu(menuConfig);
```
