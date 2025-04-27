<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>个人资料库</title>
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
        
        .knowledge-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .knowledge-card {
            background-color: white;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            padding: 20px;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .knowledge-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .knowledge-card h3 {
            margin-top: 0;
            color: #2c3e50;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
        }
        
        .knowledge-card .date {
            font-size: 0.8em;
            color: #7f8c8d;
            margin-bottom: 10px;
        }
        
        .knowledge-card .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
            margin-top: 15px;
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
            .knowledge-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>子亮的个人知识库</h1>
        <p class="subtitle">记录、整理与沉淀个人知识与经验</p>
    </header>
    
    <div class="search-container">
        <input type="text" id="search" placeholder="搜索知识条目...">
    </div>
    
    <div class="categories">
        <div class="category">全部</div>
        <div class="category">技术笔记</div>
        <div class="category">读书心得</div>
        <div class="category">生活经验</div>
        <div class="category">工作备忘</div>
        <div class="category">兴趣爱好</div>
    </div>
    
    <div class="knowledge-container">
        <div class="knowledge-card">
            <h3>如何高效学习编程</h3>
            <div class="date">2023-05-15</div>
            <p>总结了个人学习编程的有效方法，包括刻意练习、项目驱动学习和知识体系构建等...</p>
            <div class="tags">
                <span class="tag">编程</span>
                <span class="tag">学习方法</span>
                <span class="tag">技术</span>
            </div>
        </div>
        
        <div class="knowledge-card">
            <h3>《原子习惯》读书笔记</h3>
            <div class="date">2023-04-22</div>
            <p>记录书中关于习惯养成的核心观点和个人实践心得，特别是1%进步法则...</p>
            <div class="tags">
                <span class="tag">读书</span>
                <span class="tag">自我提升</span>
                <span class="tag">心理学</span>
            </div>
        </div>
        
        <div class="knowledge-card">
            <h3>家庭网络优化方案</h3>
            <div class="date">2023-03-10</div>
            <p>研究并实施的家庭网络优化方案，包括路由器选择、Mesh组网和QoS设置等...</p>
            <div class="tags">
                <span class="tag">网络</span>
                <span class="tag">技术</span>
                <span class="tag">生活</span>
            </div>
        </div>
        
        <div class="knowledge-card">
            <h3>Python数据处理技巧</h3>
            <div class="date">2023-02-28</div>
            <p>整理工作中常用的Python数据处理技巧，包括Pandas高级用法和性能优化...</p>
            <div class="tags">
                <span class="tag">Python</span>
                <span class="tag">数据处理</span>
                <span class="tag">工作</span>
            </div>
        </div>
        
        <div class="knowledge-card">
            <h3>个人财务管理方法</h3>
            <div class="date">2023-01-15</div>
            <p>实践验证有效的个人财务管理体系，包括预算制定、投资分配和消费记录等...</p>
            <div class="tags">
                <span class="tag">财务</span>
                <span class="tag">生活</span>
                <span class="tag">管理</span>
            </div>
        </div>
        
        <div class="knowledge-card">
            <h3>摄影基础知识备忘</h3>
            <div class="date">2022-12-05</div>
            <p>学习摄影过程中记录的基础知识要点，包括曝光三角、构图法则和后期技巧...</p>
            <div class="tags">
                <span class="tag">摄影</span>
                <span class="tag">爱好</span>
                <span class="tag">艺术</span>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© 2023 个人资料库 | 最后更新: <span id="last-update">2023-06-01</span></p>
    </footer>
    
    <script>
        // 简单的搜索功能
        document.getElementById('search').addEventListener('input', function(e) {
            const searchTerm = e.target.value.toLowerCase();
            const cards = document.querySelectorAll('.knowledge-card');
            
            cards.forEach(card => {
                const text = card.textContent.toLowerCase();
                if(text.includes(searchTerm)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });
        
        // 分类筛选功能
        const categories = document.querySelectorAll('.category');
        categories.forEach(category => {
            category.addEventListener('click', function() {
                const categoryName = this.textContent;
                // 这里可以添加实际的分类筛选逻辑
                alert('筛选分类: ' + categoryName);
            });
        });
        
        // 自动更新最后修改日期
        document.getElementById('last-update').textContent = new Date().toISOString().split('T')[0];
    </script>
</body>
</html>
