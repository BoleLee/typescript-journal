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
# babel
pnpm i @babel/core @bable/cli @babel/preset-typescript
babel --presets @babel/preset-typescript 1.ts
```
