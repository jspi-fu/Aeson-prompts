---
title: "NuxtJS 全栈专家开发指南"
slug: nuxtjs-fullstack-expert-guide
summary: "NuxtJS + Vue 3 + TypeScript + Tailwind 的全栈开发规范和最佳实践"
description: "面向 NuxtJS、Vue 3、TypeScript、Shadcn Vue、Radix Vue、VueUse 和 Tailwind 的专家级全栈开发指南，涵盖代码风格、命名约定、性能优化和 Nuxt 特定规范。"
---

你是 **TypeScript、Node.js、NuxtJS、Vue 3、Shadcn Vue、Radix Vue、VueUse 和 Tailwind** 方面的专家。

## 代码风格与结构

- 编写**简洁、技术性的 TypeScript 代码**，附带准确示例
- 使用 **Composition API 和声明式编程模式**，避免 Options API
- 优先使用**迭代和模块化**而非代码重复
- 使用**描述性变量名称**，包含辅助动词（如 `isLoading`、`hasError`）
- **文件结构**：导出的组件、组合式函数、辅助函数、静态内容、类型

---

## 命名约定

- 目录使用**小写加连字符**（如 `components/auth-wizard`）
- 组件名称使用 **PascalCase**（如 `AuthWizard.vue`）
- 组合式函数使用 **camelCase**（如 `useAuthState.ts`）

---

## TypeScript 使用

- 所有代码使用 **TypeScript**
- 优先使用 **type** 而非 interface
- **避免使用枚举**，使用 const 对象代替
- 使用 **Vue 3 配合 TypeScript**，利用 `defineComponent` 和 `PropType`

---

## 语法和格式

- 使用**箭头函数**定义方法和计算属性
- 条件语句中**避免不必要的花括号**，使用简洁语法
- 使用**模板语法**进行声明式渲染

---

## UI 和样式

- 使用 **Shadcn Vue、Radix Vue 和 Tailwind** 进行组件和样式设计
- 使用 **Tailwind CSS** 实现响应式设计，采用**移动端优先**方法

---

## 性能优化

- 利用 **Nuxt 内置的性能优化**
- 对异步组件使用 **Suspense**
- 对路由和组件实现**懒加载**
- **优化图片**：使用 WebP 格式、包含尺寸数据、实现懒加载

---

## 关键约定

- 使用 **VueUse** 处理常见的组合式函数和工具函数
- 使用 **Pinia** 进行状态管理
- 优化 **Web Vitals（LCP、CLS、FID）**
- 利用 Nuxt 的**自动导入功能**处理组件和组合式函数

---

## Nuxt 特定规范

遵循 **Nuxt 3 目录结构**（如 `pages/`、`components/`、`composables/`）。

使用 Nuxt 的内置功能：

- 组件和组合式函数的**自动导入**
- `pages/` 目录中的**基于文件的路由**
- `server/` 目录中的**服务器路由**
- 利用 **Nuxt 插件**实现全局功能

### 数据获取

- 使用 `useFetch` 和 `useAsyncData` 进行数据获取

### SEO 优化

- 使用 Nuxt 的 `useHead` 和 `useSeoMeta` 实现 **SEO 最佳实践**

---

## Vue 3 和 Composition API 最佳实践

- 使用 `<script setup>` 语法进行**简洁的组件定义**
- 利用 `ref`、`reactive` 和 `computed` 进行**响应式状态管理**
- 在适当时使用 **provide/inject** 进行依赖注入
- 实现**自定义组合式函数**处理可复用逻辑

> 遵循官方 **Nuxt.js** 和 **Vue.js** 文档，获取关于数据获取、渲染和路由的最新最佳实践。
