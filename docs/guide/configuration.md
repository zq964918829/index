# 基础配置

> 详细了解Docsify的各种配置选项，打造个性化的文档站点

## 🔧 核心配置

### 基本设置

在 `index.html` 文件中的 `window.$docsify` 对象中进行配置：

```javascript
window.$docsify = {
  // 站点名称
  name: 'AI文档中心',
  
  // GitHub仓库链接
  repo: 'https://github.com/your-username/ai-docsify',
  
  // 首页文件
  homepage: 'README.md',
  
  // 基础路径
  basePath: '/',
  
  // 最大内容层级
  maxLevel: 4,
  
  // 子目录最大层级
  subMaxLevel: 3,
  
  // 自动跳转到页面顶部
  auto2top: true,
  
  // 切换页面后是否自动跳转到页面顶部
  autoHeader: false
}
```

### 导航配置

```javascript
window.$docsify = {
  // 加载侧边栏
  loadSidebar: true,
  
  // 侧边栏文件名
  loadSidebar: '_sidebar.md',
  
  // 加载导航栏
  loadNavbar: true,
  
  // 导航栏文件名
  loadNavbar: '_navbar.md',
  
  // 小屏设备下合并导航栏到侧边栏
  mergeNavbar: true,
  
  // 封面页
  coverpage: true,
  
  // 封面页文件名
  coverpage: '_coverpage.md',
  
  // 只在访问主页时加载封面页
  onlyCover: false
}
```

## 🎨 外观配置

### 主题设置

```javascript
window.$docsify = {
  // 主题色
  themeColor: '#42b883',
  
  // 响应式表格
  responsiveTables: true,
  
  // 代码块主题
  themeable: {
    readyTransition: true,
    responsiveTables: true
  }
}
```

### 自定义CSS

在 `index.html` 中添加自定义样式：

```html
<style>
:root {
  /* 主题色配置 */
  --theme-color: #42b883;
  --theme-color-secondary: #369870;
  --theme-color-tertiary: #2c5530;
  
  /* 字体配置 */
  --base-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --code-font-family: 'SF Mono', Monaco, 'Cascadia Code', 'Roboto Mono', Consolas, monospace;
  
  /* 间距配置 */
  --base-line-height: 1.6;
  --base-font-size: 16px;
}

/* 侧边栏样式 */
.sidebar {
  border-right: 1px solid var(--border-color, #eee);
  background: var(--sidebar-bg, #fff);
}

/* 内容区域样式 */
.markdown-section {
  max-width: 90%;
  padding: 30px 15px 40px 15px;
}

/* 代码块样式 */
.markdown-section pre {
  background-color: var(--code-bg, #f8f8f8);
  border-radius: 6px;
}

/* 链接样式 */
.markdown-section a {
  color: var(--theme-color);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-bottom 0.3s;
}

.markdown-section a:hover {
  border-bottom-color: var(--theme-color);
}
</style>
```

## 🔍 搜索配置

### 基础搜索

```javascript
window.$docsify = {
  search: {
    // 搜索结果过期时间（毫秒）
    maxAge: 86400000,
    
    // 搜索路径
    paths: 'auto', // 或者指定具体路径 ['/', '/guide/', '/api/']
    
    // 搜索占位符
    placeholder: '🔍 搜索文档',
    
    // 无结果提示
    noData: '😞 找不到结果',
    
    // 搜索深度
    depth: 6,
    
    // 隐藏其他侧边栏内容
    hideOtherSidebarContent: false,
    
    // 搜索命名空间
    namespace: 'ai-docs'
  }
}
```

### 高级搜索配置

```javascript
window.$docsify = {
  search: {
    // 自定义搜索路径
    paths: [
      '/',
      '/guide/',
      '/api/',
      '/examples/'
    ],
    
    // 路径命名空间
    pathNamespaces: ['/zh-cn', '/ru-ru', '/de-de'],
    
    // 搜索标题层级
    depth: 3,
    
    // 最大搜索结果数
    maxResults: 20
  }
}
```

## 📋 代码配置

### 代码复制

```javascript
window.$docsify = {
  copyCode: {
    buttonText: '复制代码',
    errorText: '复制失败',
    successText: '已复制',
    
    // 复制按钮位置
    position: 'top-right', // 或 'top-left', 'bottom-right', 'bottom-left'
    
    // 显示语言标签
    showLanguage: true
  }
}
```

### 代码高亮

在HTML中引入语言支持：

```html
<!-- 基础语言支持 -->
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-bash.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-python.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-javascript.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-json.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-yaml.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-markdown.min.js"></script>

<!-- 更多语言支持 -->
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-java.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-go.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-rust.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-php.min.js"></script>
```

## 📄 分页配置

```javascript
window.$docsify = {
  pagination: {
    previousText: '上一页',
    nextText: '下一页',
    
    // 跨章节导航
    crossChapter: true,
    
    // 显示章节标题
    crossChapterText: true
  }
}
```

## 📊 统计配置

### 字数统计

```javascript
window.$docsify = {
  count: {
    countable: true,
    position: 'top',
    margin: '10px',
    float: 'right',
    fontsize: '0.9em',
    color: 'rgb(90,90,90)',
    language: 'chinese',
    localization: {
      words: '字',
      minute: '分钟'
    },
    isExpected: true
  }
}
```

## 🏷️ 标签页配置

```javascript
window.$docsify = {
  tabs: {
    persist: true,      // 记住选中的标签页
    sync: true,         // 同步所有标签页组
    theme: 'classic',   // 主题: 'classic', 'material'
    tabComments: true,  // 解析标签注释
    tabHeadings: true   // 解析标签标题
  }
}
```

## 🔗 链接配置

```javascript
window.$docsify = {
  // 外部链接目标
  externalLinkTarget: '_blank',
  
  // 外部链接关系
  externalLinkRel: 'noopener',
  
  // 路由模式
  routerMode: 'hash', // 或 'history'
  
  // 相对路径
  relativePath: false,
  
  // 404页面
  notFoundPage: true,
  
  // 404页面路径
  notFoundPage: '404.md'
}
```

## 🌐 多语言配置

```javascript
window.$docsify = {
  // 回退语言
  fallbackLanguages: ['fr', 'de'],
  
  // 语言命名空间
  nameLink: {
    '/zh-cn/': '中文',
    '/en/': 'English',
    '/': '🇺🇸'
  }
}
```

## ⚡ 性能配置

```javascript
window.$docsify = {
  // 延迟加载
  executeScript: true,
  
  // 缓存
  noEmoji: false,
  
  // 压缩
  noCompileLinks: [],
  
  // 预加载
  requestHeaders: {
    'cache-control': 'max-age=600'
  }
}
```

## 🔌 插件配置

### 图片缩放

```javascript
window.$docsify = {
  // 图片缩放配置
  zoom: {
    selector: '.markdown-section img',
    background: 'rgba(0,0,0,0.8)',
    delay: 1000,
    margin: 40,
    scrollOffset: 40
  }
}
```

### Emoji配置

```javascript
window.$docsify = {
  // 禁用emoji
  noEmoji: false
}
```

## 📱 响应式配置

```css
/* 移动端适配 */
@media screen and (max-width: 768px) {
  .sidebar {
    transform: translateX(-300px);
  }
  
  .sidebar-toggle {
    background-color: transparent;
  }
  
  .markdown-section {
    padding: 20px 10px;
  }
}

/* 平板适配 */
@media screen and (max-width: 1024px) {
  .markdown-section {
    max-width: 95%;
  }
}
```

## 🛠️ 高级配置

### 自定义钩子

```javascript
window.$docsify = {
  plugins: [
    function(hook, vm) {
      // 初始化钩子
      hook.init(function() {
        console.log('Docsify初始化完成');
      });
      
      // 页面加载前钩子
      hook.beforeEach(function(content) {
        // 在每个页面加载前执行
        return content;
      });
      
      // 页面加载后钩子
      hook.afterEach(function(html) {
        // 在每个页面加载后执行
        return html;
      });
      
      // 页面渲染完成钩子
      hook.doneEach(function() {
        // 页面渲染完成后执行
        console.log('页面渲染完成');
      });
    }
  ]
}
```

### 自定义Markdown渲染

```javascript
window.$docsify = {
  markdown: {
    smartypants: true,
    renderer: {
      code: function(code, lang) {
        // 自定义代码块渲染
        return `<pre><code class="lang-${lang}">${code}</code></pre>`;
      },
      link: function(href, title, text) {
        // 自定义链接渲染
        return `<a href="${href}" title="${title}" target="_blank">${text}</a>`;
      }
    }
  }
}
```

## 📋 配置检查清单

- [ ] 设置站点名称和描述
- [ ] 配置GitHub仓库链接
- [ ] 启用侧边栏和导航栏
- [ ] 配置搜索功能
- [ ] 设置主题色
- [ ] 启用代码复制功能
- [ ] 配置分页导航
- [ ] 添加字数统计
- [ ] 设置响应式布局
- [ ] 配置多语言支持（如需要）
- [ ] 优化移动端显示
- [ ] 测试所有功能

## 🔗 相关链接

- [主题定制](themes.md) - 深度定制主题样式
- [插件使用](plugins.md) - 探索更多实用插件
- [API参考](../api/configuration.md) - 完整的配置API文档
- [最佳实践](../writing/best-practices.md) - 配置最佳实践

---

💡 **提示**: 配置修改后记得刷新浏览器查看效果。建议在开发过程中使用浏览器的开发者工具来调试样式和功能。