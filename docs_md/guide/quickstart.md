# 快速开始

> 本指南将帮助您快速搭建和运行基于Docsify的文档系统

## 📋 前置要求

在开始之前，请确保您的系统已安装：

- **Node.js** (推荐 v14 或更高版本)
- **Git** (用于版本控制)
- **文本编辑器** (推荐 VS Code)

## 🚀 安装步骤

### 方法一：使用本项目模板

1. **克隆项目**
   ```bash
   git clone https://github.com/your-username/ai-docsify.git
   cd ai-docsify
   ```

2. **启动本地服务器**
   ```bash
   # 使用Python (如果已安装)
   python -m http.server 3000
   
   # 或使用Node.js serve包
   npx serve . -p 3000
   ```

3. **访问文档**
   打开浏览器访问 `http://localhost:3000`

### 方法二：从零开始

1. **安装Docsify CLI**
   ```bash
   npm i docsify-cli -g
   ```

2. **初始化项目**
   ```bash
   mkdir my-docs
   cd my-docs
   docsify init .
   ```

3. **启动服务**
   ```bash
   docsify serve .
   ```

## 📁 项目结构说明

```
ai-docsify/
├── index.html          # 主入口文件，包含Docsify配置
├── README.md           # 首页内容
├── _sidebar.md         # 侧边栏导航配置
├── _navbar.md          # 顶部导航栏配置
├── _coverpage.md       # 封面页配置
├── docs/               # 文档内容目录
│   ├── guide/          # 使用指南
│   ├── api/            # API文档
│   └── examples/       # 示例代码
└── assets/             # 静态资源（可选）
```

## ⚙️ 基础配置

### 修改站点信息

编辑 `index.html` 文件中的配置：

```javascript
window.$docsify = {
  name: '您的文档站点名称',
  repo: 'https://github.com/your-username/your-repo',
  // 其他配置...
}
```

### 自定义首页

编辑 `README.md` 文件来自定义首页内容：

```markdown
# 我的文档站点

> 这里是站点描述

## 特性

- 特性1
- 特性2
- 特性3
```

### 配置侧边栏

编辑 `_sidebar.md` 文件来配置导航：

```markdown
* [首页](README.md)
* [指南](guide/README.md)
  * [快速开始](guide/quickstart.md)
  * [配置](guide/configuration.md)
* [API](api/README.md)
```

## 🎨 主题定制

### 更换主题

在 `index.html` 中修改主题链接：

```html
<!-- Vue主题 (默认) -->
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@4/lib/themes/vue.css">

<!-- Buble主题 -->
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@4/lib/themes/buble.css">

<!-- Dark主题 -->
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@4/lib/themes/dark.css">

<!-- Pure主题 -->
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@4/lib/themes/pure.css">
```

### 自定义样式

在 `index.html` 的 `<style>` 标签中添加自定义CSS：

```css
:root {
  --theme-color: #42b883;  /* 主题色 */
}

.sidebar {
  border-right: 1px solid #eee;
}
```

## 🔌 常用插件

### 搜索插件

```html
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>
```

### 代码复制插件

```html
<script src="//cdn.jsdelivr.net/npm/docsify-copy-code@2"></script>
```

### 分页插件

```html
<script src="//cdn.jsdelivr.net/npm/docsify-pagination/dist/docsify-pagination.min.js"></script>
```

## 📝 编写文档

### 创建新页面

1. 在相应目录下创建 `.md` 文件
2. 在 `_sidebar.md` 中添加链接
3. 使用标准Markdown语法编写内容

### Markdown语法示例

```markdown
# 一级标题
## 二级标题
### 三级标题

**粗体文本**
*斜体文本*
`行内代码`

- 无序列表项1
- 无序列表项2

1. 有序列表项1
2. 有序列表项2

[链接文本](链接地址)
![图片描述](图片地址)

> 引用文本

```代码块```
```

## 🚀 部署上线

### GitHub Pages

1. 将代码推送到GitHub仓库
2. 在仓库设置中启用GitHub Pages
3. 选择源分支（通常是main或gh-pages）
4. 访问 `https://username.github.io/repository-name`

### Netlify

1. 连接GitHub仓库到Netlify
2. 设置构建命令（通常留空）
3. 设置发布目录为根目录 `/`
4. 部署完成后获得访问链接

## 🔧 故障排除

### 常见问题

**Q: 页面显示404错误**
A: 检查文件路径是否正确，确保文件存在

**Q: 侧边栏不显示**
A: 确保 `loadSidebar: true` 已配置，且 `_sidebar.md` 文件存在

**Q: 搜索功能不工作**
A: 确保已引入搜索插件脚本

**Q: 样式显示异常**
A: 检查主题CSS文件是否正确加载

## 📚 下一步

- [基础配置](configuration.md) - 了解更多配置选项
- [主题定制](themes.md) - 深度定制主题样式
- [插件使用](plugins.md) - 探索更多实用插件
- [最佳实践](../writing/best-practices.md) - 学习文档编写最佳实践

---

🎉 恭喜！您已成功搭建了Docsify文档系统。开始创建您的第一个文档页面吧！