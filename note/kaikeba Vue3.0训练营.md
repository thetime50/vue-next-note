# kaikeba Vue3.0训练营
https://learn.kaikeba.com/catalog/212133?type=1

## 1 环境搭建
### 1.1 环境搭建
```js

// 安装依赖
yarn --ignore-scripts
// package.json
{"dev": "node scripts/dev.js --sourcemap"}
// 打包
yarn dev
// -> ./packages/vue/dest
// packages\vue\examples\classic\todomvc.html
```


Vue.createApp() 初始化vue

- vue
  - compiler-dom
    - compiler-core
  - reactivity
  - runtime-dom
    - runtime-core

### 1.2 

打包过程：
- [dev.js](../scripts/dev.js)  
- [rollup.config.js](../rollup.config.js)
- [入口文件 packages/vue/src/index.js](../packages/vue/src/index.ts)

### 1.3 Vue.createApp发生了什么
[deml page](../packages\vue\examples\01-init.html)

- \[reveal in sideber\] -> [runtime-dom/src/index.ts](../packages/runtime-dom/src/index.ts)
- [runtime-core -> createRenderer](../packages\runtime-core\src\renderer.ts)  
- [createApp: createAppAPI](../packages\runtime-core\src\apiCreateApp.ts)

ctrl+k+\[ 折叠所有

### 1.4 互动
vue3 composition 写法没有this 兼容vue2的 option写法有this

```
componentEffect (renderer.ts:1350)
reactiveEffect (effect.ts:95)
effect (effect.ts:64)
setupRenderEffect (renderer.ts:1349)
mountComponent (renderer.ts:1288)
processComponent (renderer.ts:1221)
patch (renderer.ts:514)
render (renderer.ts:2205)
mount (apiCreateApp.ts:247)
app.mount (index.ts:70)
(anonymous) (01-init.html:26)
```

2020年10月21日 23点16分 (1:11:57)

//todo git提交信息格式 scripts\verifyCommit.js 
