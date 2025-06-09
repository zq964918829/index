# AI文档中心

> 一个基于Docsify构建的现代化文档查看系统

## 🚀 特性

- **📱 响应式设计** - 完美适配桌面端和移动端
- **🔍 全文搜索** - 快速查找所需内容
- **🎨 美观主题** - 现代化的Vue主题风格
- **📝 Markdown支持** - 原生支持Markdown语法
- **🔗 代码高亮** - 支持多种编程语言语法高亮
- **📋 一键复制** - 代码块一键复制功能
- **📊 字数统计** - 实时显示文档字数和阅读时间
- **🏷️ 标签页** - 支持标签页形式的内容组织
- **🖼️ 图片缩放** - 点击图片可放大查看
- **😊 Emoji支持** - 原生支持Emoji表情

## 📖 快速开始

### 本地运行

1. **克隆项目**
   ```bash
   git clone <your-repo-url>
   cd ai-docsify
   ```

2. **启动本地服务器**
   ```bash
   # 使用Python
   python -m http.server 3000
   
   # 或使用Node.js
   npx serve .
   
   # 或使用docsify-cli
   npm i docsify-cli -g
   docsify serve .
   ```

3. **访问文档**
   打开浏览器访问 `http://localhost:3000`

### 在线部署

支持部署到以下平台：
- GitHub Pages
- Netlify
- Vercel
- 任何静态网站托管服务

## 📁 项目结构

```
ai-docsify/
├── index.html          # 主入口文件
├── README.md           # 首页内容
├── _sidebar.md         # 侧边栏配置
├── _navbar.md          # 导航栏配置
├── _coverpage.md       # 封面页配置
├── docs/               # 文档目录
│   ├── guide/          # 使用指南
│   ├── api/            # API文档
│   └── examples/       # 示例代码
└── assets/             # 静态资源
    ├── images/         # 图片资源
    └── css/            # 自定义样式
```

## ✨ 功能展示

### 代码高亮

```javascript
/**
 * 示例JavaScript代码
 * 展示代码高亮功能
 */
function greetUser(name) {
    console.log(`Hello, ${name}! 欢迎使用AI文档中心`);
    return `Welcome to AI Docs, ${name}!`;
}

// 调用函数
greetUser('开发者');
```

```python
# Python代码示例
def calculate_fibonacci(n):
    """
    计算斐波那契数列的第n项
    """
    if n <= 1:
        return n
    return calculate_fibonacci(n-1) + calculate_fibonacci(n-2)

# 计算前10项
for i in range(10):
    print(f"F({i}) = {calculate_fibonacci(i)}")
```

### 表格支持

| 功能 | 描述 | 状态 |
|------|------|------|
| 搜索 | 全文搜索功能 | ✅ 已实现 |
| 主题 | 多主题切换 | ✅ 已实现 |
| 响应式 | 移动端适配 | ✅ 已实现 |
| 插件 | 丰富的插件生态 | ✅ 已实现 |

### 提示框

> [!NOTE]
> 这是一个信息提示框，用于显示重要信息。

> [!TIP]
> 这是一个技巧提示框，分享有用的小贴士。

> [!WARNING]
> 这是一个警告提示框，提醒用户注意事项。

## 🛠️ 自定义配置

### 修改主题色

在 `index.html` 中修改CSS变量：

```css
:root {
  --theme-color: #42b883;  /* 主题色 */
  --theme-color-secondary: #369870;  /* 次要主题色 */
}
```

### 添加新页面

1. 在相应目录下创建 `.md` 文件
2. 在 `_sidebar.md` 中添加链接
3. 内容会自动渲染

## 📚 文档编写指南

### Markdown语法

支持标准Markdown语法，包括：
- 标题 (H1-H6)
- 列表 (有序/无序)
- 链接和图片
- 代码块
- 表格
- 引用
- 分割线

### 扩展语法

#### 标签页

<!-- tabs:start -->

#### **JavaScript**

```javascript
console.log('Hello from JavaScript!');
```

#### **Python**

```python
print('Hello from Python!')
```

#### **Bash**

```bash
echo "Hello from Bash!"
```

<!-- tabs:end -->

## 🤝 贡献指南

欢迎贡献代码和文档！请遵循以下步骤：

1. Fork 本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🙏 致谢

- [Docsify](https://docsify.js.org/) - 优秀的文档生成工具
- [Vue.js](https://vuejs.org/) - 提供美观的主题样式
- 所有贡献者和用户的支持

---

**开始探索文档吧！** 👈 使用左侧导航栏浏览不同章节。