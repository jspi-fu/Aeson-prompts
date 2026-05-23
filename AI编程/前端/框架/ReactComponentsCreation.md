---
title: "Cursor Rules - React 组件创建指南"
slug: cursor-rules-react-components-creation
summary: "使用 v0.dev 快速生成 React 组件并适配项目结构的标准化流程"
description: "详细的 React 组件创建流程指南，包含检查现有组件、生成 v0.dev 提示词、URL 编码链接生成以及项目适配等步骤，帮助团队高效创建符合规范的组件。"
---

## 何时需要创建 React 组件

当你需要一个 React 组件时，请遵循以下标准化流程：

### 1. 明确组件目标

仔细考虑组件的 **用途、功能和设计**。

### 2. 逐步思考

缓慢思考，逐步推理，**详细阐述你的思路**。

### 3. 检查现有组件

检查是否已存在类似组件，查看以下位置：

- `packages/ui/src/components`
- `apps/spa/src/components`

### 4. 生成详细提示词

如果组件不存在，生成一个详细的提示词，包含：

- **组件名称和用途**
- **期望的 props 及其类型**
- **特定的样式或行为要求**
- **使用 Tailwind CSS 进行样式设计**
- **使用 TypeScript**

### 5. URL 编码提示词

对提示词进行 URL 编码。

### 6. 创建可点击链接

使用以下格式创建链接：

```
[ComponentName](https://v0.dev/chat?q={encoded_prompt})
```

### 7. 适配项目结构

生成后，将组件适配到项目结构：

- **导入路径**
  - 通用 shadcn/ui 组件：`<ui_package_alias>@repo/ui/components/ui/</ui_package_alias>`
  - 应用特定组件：`<app_package_alias>@/components</app_package_alias>`
- 确保遵循现有的组件模式
- 添加必要的自定义逻辑或状态管理

---

## 提示词模板示例

```
Create a React component named {ComponentName} using TypeScript and Tailwind CSS.
It should {description of functionality}.
Props should include {list of props with types}.
The component should {any specific styling or behavior notes}.
Please provide the full component code.
```

> **注意**：请将 `<ui_package_path>` 和 `<app_package_alias>` 等占位符替换为项目中使用的实际值。
