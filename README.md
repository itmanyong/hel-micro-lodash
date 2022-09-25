# hel-micro-lodash
[前往 npm](https://www.npmjs.com/package/hel-micro-lodash)
[前往 github](https://github.com/itmanyong/hel-micro-lodash)

## 使用

1.安装 hel-micro 依赖包

```js
pnpm add hel-micro
```

2.预加载主包

```js
// 安装主包
pnpm add hel-micro-lodash
// 在使用之前加载主包
import { preFetchLib } from 'hel-micro'
await preFetchLib('hel-micro-lodash', { versionId:'版本号' });// 忽略版本号将默认获取最新版本
// 后续使用
import helLodash from 'hel-micro-lodash';
helLodash.apiName()
```

3.懒加载主包

```js
// 后续再次加载会直接复用
const helLodashLib = await preFetchLib("hel-micro-lodash", { versionId:'版本号' });// 忽略版本号将默认获取最新版本
helLodashLib.apiName();
```

## 其他

1.将 lodash 通过 hel-micro 的方式进行提供，包含所有 lodash 导出 2.版本号与 lodash 保持一致，尾号为包更新版本号
2.[hel-micro](https://github.com/tnfe/hel)
