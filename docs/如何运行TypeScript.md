# 如何运行TypeScript

Chrome, Node暂不支持直接运行，可通过Deno运行，此过程是进行了类型擦除。

## 如何擦除类型

```bash
# 1)快（不检查TS语法）
# esbuild
npm i -g esbuild
esbuild 1.ts > 1.js
# swc
npm i -g @swc/cli @swc/core
swc 1.ts -o 1.js
# 2）慢
# tsc
npm i -g typescript
tsc 1.ts
# babel 项目内安装
pnpm add @babel/core @babel/cli @babel/preset-typescript # 先安装依赖
babel --presets @babel/preset-typescript 1.ts # 将此命令写在package.json运行脚本中
./node_modules/.bin/babel --presets @babel/preset-typescript 1.ts # 使用相对路径访问babel命令行
npx babel --presets @babel/preset-typescript 1.ts # 执行之前首先要安装 @babel/cli 和 @babel/core
```

- [安装pnpm](https://www.pnpm.cn/installation)
- [@babel/preset-typescript](https://www.babeljs.cn/docs/babel-preset-typescript)
- [@babel/cli](https://www.babeljs.cn/docs/babel-cli)

## ES6兼容表

[es6 compatebility table](https://kangax.github.io/compat-table/es6/)

## 在线编辑器

- [TypeScript playground](https://www.typescriptlang.org/play)
- [Playcode.io](https://playcode.io/) 实时预览很快，收费
- [Stackblitz.com](https://stackblitz.com/) 有单独的vite分类，界面跟VSCode很一致
- [Codesandbox.io](https://codesandbox.io/)

## 使用vite运行TypeScript

## 如何用Node运行TS
