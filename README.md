# app-vue3-vite

vite 搭建 vue3 + ts 初始化模板。

## 流程

当配置 `vite.config.ts` 时，因为找不到 `path` 模块，所以安装了依赖 `yarn add -D @types/node`。
```ts
// vite.config.ts
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'
import { resolve } from 'path'

export default defineConfig({
  plugins: [vue()],
  resolve: {
    alias: {
      '@': resolve(__dirname, 'src'), // 设置 @ 指向 src 目录
    }
  },
  base: './', // 设置打包路径
})
```

