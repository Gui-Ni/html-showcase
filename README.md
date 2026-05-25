# 分析报告展示站

一个轻量级的 HTML 报告管理 + 在线预览工具，支持本地模式和 GitHub Pages 模式。

---

## 目录结构

```
html-showcase/
├── index.html              ← 展示站入口（部署到 GitHub Pages）
├── README.md               ← 本文档
├── 厨房用品/               ← 把 HTML 报告丢进这里
├── 户外灯具/
├── 投资研究/
└── _assets/                ← 公共资源（如有）
```

---

## 使用方法

### 方式一：本地直接打开

双击 `index.html` 即可在浏览器中查看，已自动加载示例文件。

### 方式二：部署到 GitHub Pages（推荐）

1. 在 GitHub 新建一个 **公开** 仓库，如 `html-showcase`
2. 把 `html-showcase` 文件夹里的内容全部 push 到仓库的 **根目录**
3. 进入仓库 **Settings → Pages → Source**，选择 `main` 分支和 `/ (root)`，点击 Save
4. 等 1-2 分钟，访问 `https://你的用户名.github.io/html-showcase/`

> GitHub Actions 会自动配置好（`.github/workflows/pages.yml` 已包含）

---

## 添加新报告

直接把 HTML 文件丢进对应的项目文件夹即可，刷新页面后自动显示：

- `厨房用品/` → 电陶炉、塔吉锅、除螨仪相关分析
- `户外灯具/` → ecna 小灯、odmb 大灯、Mancra 路径灯等
- `投资研究/` → 股票、机器人产业链等分析报告

---

## 连接到 GitHub（进阶）

在展示站顶部输入 `owner/repo`，点击「连接 GitHub」，即可从仓库实时读取文件列表，无需手动更新。

> 首次使用需要在 GitHub Settings → Developer settings → Personal access tokens 生成一个 token，勾选 `repo` 权限。

---

## 快捷键

| 操作 | 快捷键 |
|------|--------|
| 关闭预览 | `Esc` |
| 新窗口打开 | 点击右上角「↗ 新窗口」 |

---

## 自定义项目分类

编辑 `index.html`，在 `LOCAL_FILES` 数组中新增文件条目，或修改 `FOLDER_ICONS` 对象添加新的项目分类。

---

## 已在库的 HTML 报告

| 文件名 | 项目 | 类型 |
|--------|------|------|
| competitive_analysis.html | 厨房用品 | 📊 竞品分析 |
| hepa_filter_analysis.html | 厨房用品 | 📊 HEPA VOC分析 |
| hepa_filter_pricing.html | 厨房用品 | 💰 HEPA定价 |
| pricing_simulator_v3.html | 厨房用品 | 💰 定价模拟器 |
