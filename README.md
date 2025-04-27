<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>个人资料库</title>
    <!-- 引入Markdown解析库 -->
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        
        header {
            background-color: #2c3e50;
            color: white;
            padding: 20px;
            border-radius: 5px;
            margin-bottom: 30px;
        }
        
        h1 {
            margin: 0;
        }
        
        .subtitle {
            font-style: italic;
            opacity: 0.8;
        }
        
        .search-container {
            margin: 20px 0;
        }
        
        #search {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        
        .categories {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 30px;
        }
        
        .category {
            background-color: #3498db;
            color: white;
            padding: 10px 15px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .category:hover {
            background-color: #2980b9;
        }
        
        .doc-container {
            display: grid;
            grid-template-columns: 250px 1fr;
            gap: 20px;
        }
        
        .sidebar {
            background-color: white;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            padding: 15px;
            height: fit-content;
        }
        
        .doc-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .doc-item {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
            cursor: pointer;
        }
        
        .doc-item:hover {
            color: #3498db;
        }
        
        .doc-content {
            background-color: white;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            padding: 30px;
        }
        
        .doc-content img {
            max-width: 100%;
        }
        
        .doc-meta {
            display: flex;
            justify-content: space-between;
            color: #7f8c8d;
            font-size: 0.9em;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .doc-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
            margin-top: 20px;
        }
        
        .tag {
            background-color: #ecf0f1;
            color: #7f8c8d;
            padding: 3px 8px;
            border-radius: 3px;
            font-size: 0.8em;
        }
        
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            color: #7f8c8d;
            font-size: 0.9em;
        }
        
        @media (max-width: 768px) {
            .doc-container {
                grid-template-columns: 1fr;
            }
            
            .sidebar {
                order: 2;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>个人资料库</h1>
        <p class="subtitle">Markdown 格式的个人知识管理与文档存储</p>
    </header>
    
    <div class="search-container">
        <input type="text" id="search" placeholder="搜索文档...">
    </div>
    
    <div class="categories">
        <div class="category active">全部文档</div>
        <div class="category">技术文档</div>
        <div class="category">学习笔记</div>
        <div class="category">生活记录</div>
        <div class="category">工作资料</div>
    </div>
    
    <div class="doc-container">
        <div class="sidebar">
            <h3>文档列表</h3>
            <ul class="doc-list" id="docList">
                <li class="doc-item" data-file="tech-guide.md">技术指南</li>
                <li class="doc-item" data-file="learning-notes.md">学习笔记</li>
                <li class="doc-item" data-file="travel-log.md">旅行日志</li>
                <li class="doc-item" data-file="work-process.md">工作流程</li>
                <li class="doc-item" data-file="book-summary.md">读书摘要</li>
            </ul>
        </div>
        
        <div class="doc-content" id="docContent">
            <div class="doc-meta">
                <span id="docTitle">欢迎使用个人资料库</span>
                <span id="docDate"></span>
            </div>
            <div id="markdownContent">
                <h2>个人资料库使用说明</h2>
                
                <p>这是一个基于 Markdown 的个人资料管理系统，适合存储和管理各种个人文档。</p>
                
                <h3>主要功能</h3>
                <ul>
                    <li>支持 Markdown 格式文档展示</li>
                    <li>文档分类管理</li>
                    <li>全文搜索功能</li>
                    <li>响应式设计，适配各种设备</li>
                </ul>
                
                <h3>如何使用</h3>
                <ol>
                    <li>在左侧选择要查看的文档</li>
                    <li>文档内容将以 Markdown 格式渲染显示</li>
                    <li>使用顶部搜索框可以快速查找文档</li>
                    <li>点击分类标签可以筛选文档</li>
                </ol>
                
                <h3>Markdown 文档规范</h3>
                <p>建议按照以下格式创建您的 Markdown 文档：</p>
                
                ```markdown
                # 文档标题
                
                > 创建时间: 2023-06-01 | 最后更新: 2023-06-15
                
                ## 概述
                文档的简要说明...
                
                ## 详细内容
                - 列表项1
                - 列表项2
                
                ```代码示例```
                
                ## 参考资料
                1. [相关链接](https://example.com)
                ```
                
                <div class="doc-tags">
                    <span class="tag">帮助</span>
                    <span class="tag">文档</span>
                    <span class="tag">指南</span>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© 2023 个人资料库 | 使用 Markdown 格式存储 | 最后更新: <span id="last-update">2023-06-01</span></p>
    </footer>
    
    <script>
        // 文档数据 - 实际使用中可以替换为从服务器加载
        const documents = {
            "tech-guide.md": `# 技术指南文档示例

> 创建时间: 2023-05-10 | 最后更新: 2023-05-20

## 常用命令备忘

\`\`\`bash
# 查看系统信息
uname -a

# 查看磁盘空间
df -h

# 查找文件
find /path -name "*.md"
\`\`\`

## 开发工具配置

1. **VS Code 设置**
   - 推荐插件:
     - Markdown All in One
     - Prettier
     - ESLint

2. **Git 配置**
   - 常用别名:
   \`\`\`gitconfig
   [alias]
       co = checkout
       br = branch
       ci = commit
   \`\`\`

<div class="doc-tags">
    <span class="tag">技术</span>
    <span class="tag">备忘</span>
    <span class="tag">开发</span>
</div>`,
            
            "learning-notes.md": `# 学习笔记示例

> 创建时间: 2023-04-15 | 最后更新: 2023-04-25

## 机器学习要点

### 监督学习
- 线性回归
- 逻辑回归
- 支持向量机

### 无监督学习
- K-means聚类
- 主成分分析(PCA)

## 数学公式示例

行内公式: $E=mc^2$

块级公式:

$$
\\nabla \\cdot \\mathbf{D} = \\rho
$$

<div class="doc-tags">
    <span class="tag">学习</span>
    <span class="tag">笔记</span>
    <span class="tag">AI</span>
</div>`
        };

        // 初始化Markdown渲染
        marked.setOptions({
            breaks: true,
            gfm: true
        });

        // 文档点击事件
        document.querySelectorAll('.doc-item').forEach(item => {
            item.addEventListener('click', function() {
                const fileName = this.getAttribute('data-file');
                loadDocument(fileName);
                
                // 更新活动状态
                document.querySelectorAll('.doc-item').forEach(i => i.classList.remove('active'));
                this.classList.add('active');
            });
        });

        // 加载文档函数
        function loadDocument(fileName) {
            const contentDiv = document.getElementById('markdownContent');
            const titleSpan = document.getElementById('docTitle');
            const dateSpan = document.getElementById('docDate');
            
            if (documents[fileName]) {
                // 从内存中加载文档
                contentDiv.innerHTML = marked.parse(documents[fileName]);
                
                // 提取标题和日期
                const titleMatch = documents[fileName].match(/^# (.+)/m);
                const dateMatch = documents[fileName].match(/最后更新: (.+)/);
                
                titleSpan.textContent = titleMatch ? titleMatch[1] : fileName;
                dateSpan.textContent = dateMatch ? dateMatch[1] : '';
            } else {
                // 实际使用中可以替换为从服务器加载Markdown文件
                fetch(fileName)
                    .then(response => response.text())
                    .then(text => {
                        contentDiv.innerHTML = marked.parse(text);
                        
                        // 提取标题和日期
                        const titleMatch = text.match(/^# (.+)/m);
                        const dateMatch = text.match(/最后更新: (.+)/);
                        
                        titleSpan.textContent = titleMatch ? titleMatch[1] : fileName;
                        dateSpan.textContent = dateMatch ? dateMatch[1] : '';
                    })
                    .catch(err => {
                        contentDiv.innerHTML = `<p>无法加载文档: ${fileName}</p><p>${err.message}</p>`;
                        titleSpan.textContent = "加载错误";
                        dateSpan.textContent = "";
                    });
            }
        }

        // 搜索功能
        document.getElementById('search').addEventListener('input', function(e) {
            const term = e.target.value.toLowerCase();
            const items = document.querySelectorAll('.doc-item');
            
            items.forEach(item => {
                if (item.textContent.toLowerCase().includes(term)) {
                    item.style.display = 'block';
                } else {
                    item.style.display = 'none';
                }
            });
        });

        // 分类筛选
        document.querySelectorAll('.category').forEach(cat => {
            cat.addEventListener('click', function() {
                document.querySelectorAll('.category').forEach(c => c.classList.remove('active'));
                this.classList.add('active');
                
                // 这里可以添加实际的分类筛选逻辑
                const category = this.textContent;
                console.log(`筛选分类: ${category}`);
            });
        });

        // 更新最后修改日期
        document.getElementById('last-update').textContent = new Date().toISOString().split('T')[0];
    </script>
</body>
</html>
