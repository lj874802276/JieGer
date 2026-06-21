# JieGer 个人主页

> HarmonyOS 独立开发者的数字名片 — 少即是多，慢即是快。

[![GitHub](https://img.shields.io/badge/GitHub-JieGer-3B5BDB?logo=github)](https://github.com/lj874802276/JieGer)
[![HarmonyOS](https://img.shields.io/badge/HarmonyOS-Native-blue?logo=huawei)](https://developer.harmonyos.com)

## 在线预览

[https://jieger.pages.dev](https://jieger.pages.dev)（待部署）

## 项目简介

这是一个极简优雅的个人开发者主页，专为 HarmonyOS 独立开发者打造。零构建依赖，纯静态 HTML/CSS/JS，双击即用，支持直接部署到任何静态托管平台。

**核心定位**：用理念驱动鸿蒙原生应用，追求克制、专注与长期价值。

## 技术栈

- **前端**：原生 HTML5 + CSS3 + JavaScript（零框架）
- **设计**：极简风格，鸿蒙蓝强调色，系统原生字体栈
- **部署**：Cloudflare Pages / GitHub Pages / 任意静态托管

## 项目结构

```
.
├── index.html          # 首页（个人介绍 + 精选作品）
├── projects.html       # 作品集（4 个 HarmonyOS 应用）
├── notes.html          # 技术笔记（预留入口）
├── 404.html            # 自定义 404 页面
├── css/
│   ├── style.css       # 全局样式 + 首页样式
│   └── page.css        # 子页面通用样式
├── js/
│   └── main.js         # 主题切换 + 邮箱复制 + 滚动动画
└── images/
    ├── project-food.webp     # 今天吃啥饭（元服务）
    ├── project-todo.webp     # 鸿蒙待办
    ├── project-expense.webp  # 轻记账
    └── project-focus.webp    # 专注时钟
```

## 核心特性

| 特性 | 说明 |
| :--- | :--- |
| 主题切换 | 自动跟随系统偏好，支持手动切换，记忆用户选择 |
| 滚动渐入 | IntersectionObserver 驱动的 fade-in 动画 |
| 邮箱复制 | 一键复制到剪贴板，带 Toast 提示 |
| 双格式图片 | `<picture>` 标签优先 WebP，自动回退 JPG |
| 安全策略 | CSP / X-Frame-Options / Referrer Policy 全链路防护 |
| 打印友好 | 隐藏装饰元素，保留核心内容 |
| 无障碍 | 完整 ARIA 标签，键盘导航，WCAG AA 对比度 |

## 开发理念

1. **尊重系统原生体验** — 不强行移植 iOS/Android 逻辑，深度融入 HarmonyOS 设计规范
2. **克制与专注** — 每个功能都有明确目的，拒绝"为了创新而创新"
3. **隐私优先** — 默认最小权限，数据本地处理，透明可控
4. **为长期使用而构建** — 代码可维护、架构可演进，不追求短期交付

## 作品展示

| 项目 | 类型 | 简介 |
| :--- | :--- | :--- |
| **今天吃啥饭** | 元服务 | 无需安装、即用即走，随机推荐菜品解决选择困难 |
| **鸿蒙待办** | 原生应用 | ArkTS 开发的待办管理，支持本地持久化与卡片形态 |
| **轻记账** | 原生应用 | 隐私优先的本地记账工具，零权限、完全离线 |
| **专注时钟** | 原生应用 | 基于番茄工作法的时间管理，极简无干扰 |

## 本地运行

```bash
# 任意静态服务器
python -m http.server 8000

# 或 Node.js
npx serve .
```

## 部署

### Cloudflare Pages（推荐）

1. Fork 本仓库到 GitHub
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com)
3. Workers & Pages → Create application → Connect to Git
4. 选择仓库，Framework preset: **None**，Build command: **留空**
5. Save and Deploy

### 直接上传

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com)
2. Workers & Pages → Create application → Upload assets
3. 拖拽项目文件夹，直接部署

## 性能指标

- 首屏请求数：**3 个**（HTML + CSS + JS）
- 图片体积：**WebP 平均节省 69%**
- 外部依赖：**0**
- Lighthouse 目标：Performance ≥ 95, Accessibility ≥ 95, SEO ≥ 95

## 开源协议

MIT License © 2026 JieGer
