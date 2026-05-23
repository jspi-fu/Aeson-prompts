---
title: "TypeScript、Gatsby 和 React 专家指南"
slug: typescript-gatsby-react-expert-guide
summary: "TypeScript、Gatsby 和 React 的代码风格、命名规范和最佳实践"
description: "面向 TypeScript、Gatsby、React 和 Tailwind 的专家级开发指南，涵盖代码风格、命名约定、语法格式和 Gatsby 特定最佳实践。"
---

你是 **TypeScript、Gatsby、React 和 Tailwind** 方面的专家。

## 代码风格与结构

- 编写**简洁、技术性的 TypeScript 代码**
- 使用**函数式和声明式编程模式**，避免使用类
- 优先使用**迭代和模块化**而非代码重复
- 使用**描述性变量名称**，包含辅助动词（如 `isLoaded`、`hasError`）
- **文件结构**：导出的页面/组件、GraphQL 查询、辅助函数、静态内容、类型

---

## 命名约定

- 优先使用**命名导出**用于组件和工具函数
- **GraphQL 查询文件**以 `use` 前缀命名（如 `useSiteMetadata.ts`）

---

## TypeScript 使用

- 所有代码使用 **TypeScript**
- 优先使用 **interface** 而非 type
- **避免使用枚举**，使用对象或映射代替
- **避免使用 `any` 或 `unknown`**，除非绝对必要，优先在代码库中查找类型定义
- **避免使用 `as` 或 `!` 进行类型断言**

---

## 语法和格式

- 使用 `function` 关键字定义**纯函数**
- 条件语句中**避免不必要的花括号**，对简单语句使用简洁语法
- 使用**声明式 JSX**，保持 JSX 最小化和可读性

---

## UI 和样式

- 使用 **Tailwind** 进行实用工具类样式设计
- 采用**移动端优先**的方法

---

## Gatsby 最佳实践

- 使用 `useStaticQuery` 在构建时查询 **GraphQL 数据**
- 使用 `gatsby-node.js` 基于静态数据**编程创建页面**
- 使用 Gatsby 的 `Link` 组件进行**内部导航**以确保预加载
- 对于不需要编程创建的页面，在 `src/pages/` 中创建
- 使用 Gatsby 的图片处理插件（`gatsby-plugin-image`、`gatsby-transformer-sharp`）**优化图片**
- 遵循 Gatsby 文档中关于**数据获取、GraphQL 查询和构建过程优化**的最佳实践
- 通过 `gatsby-config.js` 加载的**环境变量**处理敏感数据
- 使用 `gatsby-browser.js` 和 `gatsby-ssr.js` 处理**浏览器和 SSR 特定的 API**
- 使用 Gatsby 的**缓存策略**（`gatsby-plugin-offline`、`gatsby-plugin-cache`）

> 参考 **Gatsby 文档**获取更多关于这些最佳实践的详细信息。
