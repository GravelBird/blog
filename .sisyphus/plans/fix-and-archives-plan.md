# 修复与实施计划 v2

## 当前状态分析

### 已完成（保留）
1. ✅ **热图功能** - `contribute-heatmap.html` 已存在并在 `list.html` 中引用
2. ✅ **首页布局** - `list.html` 保持不变，热图在第55-57行
3. ✅ **主题** - 使用 hugo-PaperMod，配色和框架保持不变
4. ✅ **文章布局** - `single.html` 保持不变，带 TOC 侧边栏

### 待完成
1. ❌ **归档页面布局** - 缺少 `layouts/_default/archives.html`
2. ❌ **构建错误** - TOC sidebar 有语法错误需要修复

## 实施步骤

### 步骤 1: 修复 TOC Sidebar 语法错误
- **问题**: `toc-sidebar.html` 可能存在语法问题导致构建失败
- **操作**: 检查并修复该文件

### 步骤 2: 创建归档页面布局
- **文件**: `layouts/_default/archives.html`
- **参考**: 从 hugo-PaperMod 主题复制并适配
- **样式**: 使用 PaperMod 内置 CSS，不添加新样式

### 步骤 3: 验证
- Hugo 构建成功
- 首页热图正常显示
- 归档页面正常显示
- 文章页面 TOC 正常

## 文件清单

### 需要修改的文件
1. `layouts/partials/toc-sidebar.html` - 修复语法错误

### 需要创建的文件
1. `layouts/_default/archives.html` - 归档页面布局

### 保持不变的文件
1. `layouts/_default/list.html` - 首页布局（包含热图）
2. `layouts/_default/single.html` - 文章布局
3. `layouts/partials/contribute-heatmap.html` - 热图组件
4. `hugo.toml` - 配置
5. 所有 CSS/JS 资源
