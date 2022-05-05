# app-vue3-vite

vite 搭建 vue3 + ts 初始化模板。

## 配置 `vite.config.ts`

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
    },
  },
  base: './', // 设置打包路径
})
```

## 代码规范

### Eslint

```sh
$ yarn add -D eslint eslint-plugin-vue vue-eslint-parser @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint-config-airbnb-base eslint-plugin-import eslint-import-resolver-alias
```

[Does not work well with \<script setup\>](https://eslint.vuejs.org/user-guide/#does-not-work-well-with-script-setup)

## 单元测试

```sh
$ yarn add -D jest @vue/test-utils@next @vue/vue3-jest ts-jest @types/jest eslint-plugin-jest
```

详情请看 `tsconfig.json` 和 `jest.config.js` 配置文件。

## 打包出现问题

1. 可能是 `vue-tsc` 版本和当前 `vscode` 编辑器安装的 `volar` 插件版本不一致。更新 `yarn add -D vue-tsc` 即可。
