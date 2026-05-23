---
title: Django 开发规范
slug: django
summary: Django 与可扩展 Web 应用的开发规范，涵盖 MVT 模式、ORM 实践、错误处理、性能优化和安全最佳实践。
description: 一份面向 Django 项目的工程规范，包括编码风格、CBV/FBV 选择、ORM 使用、表单验证、错误处理、依赖管理、性能优化（缓存、异步、索引）以及安全与测试要求。
---

## 核心原则

- 编写清晰、技术精确的 Django 示例代码。
- 优先使用 Django 内置特性和工具。
- 遵循 **PEP 8** 编码风格，注重可读性和可维护性。
- 使用描述性的变量和函数命名（小写加下划线）。
- 以 **Django App** 为单位组织项目，促进复用和关注点分离。

## Django/Python 实践

- 复杂视图使用**基于类的视图（CBV）**；简单逻辑优先使用**基于函数的视图（FBV）**。
- 利用 Django ORM 进行数据库交互；除非性能必需，避免原生 SQL。
- 使用 Django 内置用户模型和认证框架进行用户管理。
- 利用 Django 表单和模型表单类处理表单验证。
- 严格遵循 **MVT（Model-View-Template）** 模式实现关注点分离。
- 审慎使用中间件处理横切关注点（认证、日志、缓存）。

## 错误处理与验证

- 在视图层实现错误处理，使用 Django 内置错误处理机制。
- 使用 Django 验证框架验证表单和模型数据。
- 业务逻辑和视图中优先使用 `try-except` 块处理异常。
- 自定义错误页面（如 404、500）提升用户体验并提供有用信息。
- 使用 **Django signals** 将错误处理和日志与核心业务逻辑解耦。

## 依赖项

| 依赖 | 用途 |
|------|------|
| Django | Web 框架 |
| Django REST Framework | API 开发 |
| Celery | 后台任务 |
| Redis | 缓存与任务队列 |
| PostgreSQL / MySQL | 生产数据库 |

## Django 专项指南

- 使用 Django 模板渲染 HTML，使用 DRF 序列化器返回 JSON。
- 业务逻辑放在模型和表单中；视图保持轻量，专注于请求处理。
- 使用 Django URL 调度器（`urls.py`）定义清晰的 RESTful URL 模式。
- 遵循 Django 安全最佳实践：CSRF 防护、SQL 注入防护、XSS 防护。
- 使用 Django 内置测试工具（`unittest` 和 `pytest-django`）确保代码质量。
- 利用 Django 缓存框架优化高频访问数据的性能。
- 使用中间件处理通用任务（认证、日志、安全）。

## 性能优化

- 使用 Django ORM 的 `select_related` 和 `prefetch_related` 优化关联对象查询。
- 使用 Django 缓存框架配合后端（Redis 或 Memcached）减少数据库负载。
- 实施数据库索引和查询优化技术提升性能。
- 使用异步视图和后台任务（通过 Celery）处理 I/O 密集型或长时间运行的操作。
- 使用 Django 静态文件管理系统（如 WhiteNoise 或 CDN 集成）优化静态文件处理。

## 关键约定

1. 遵循 Django 的"约定优于配置"原则，减少样板代码。
2. 在开发的每个阶段优先考虑安全性和性能优化。
3. 保持清晰、逻辑的项目结构以增强可读性和可维护性。
