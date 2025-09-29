<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>三列布局文档</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei', sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f5f5f5;
        }
        
        .container {
            display: flex;
            min-height: 100vh;
            max-width: 1600px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 20px rgba(0,0,0,0.05);
        }
        
        /* 左侧目录栏 */
        .sidebar-left {
            width: 250px;
            padding: 30px 20px;
            background: #fafafa;
            border-right: 1px solid #e0e0e0;
            position: sticky;
            top: 0;
            height: 100vh;
            overflow-y: auto;
        }
        
        .toc-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #2c3e50;
            padding-bottom: 10px;
            border-bottom: 2px solid #3498db;
        }
        
        .toc-list {
            list-style: none;
        }
        
        .toc-list li {
            margin-bottom: 8px;
        }
        
        .toc-list a {
            color: #555;
            text-decoration: none;
            display: block;
            padding: 5px 10px;
            border-radius: 4px;
            transition: all 0.3s ease;
        }
        
        .toc-list a:hover {
            background: #e8f4fd;
            color: #3498db;
            transform: translateX(5px);
        }
        
        .toc-list .toc-h2 {
            padding-left: 20px;
            font-size: 14px;
        }
        
        .toc-list .toc-h3 {
            padding-left: 40px;
            font-size: 13px;
            color: #666;
        }
        
        /* 中间内容区 */
        .content {
            flex: 1;
            padding: 40px 50px;
            max-width: 800px;
        }
        
        .content h1 {
            font-size: 32px;
            margin-bottom: 30px;
            color: #2c3e50;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
        }
        
        .content h2 {
            font-size: 24px;
            margin-top: 30px;
            margin-bottom: 15px;
            color: #34495e;
            padding-left: 10px;
            border-left: 4px solid #3498db;
        }
        
        .content h3 {
            font-size: 18px;
            margin-top: 20px;
            margin-bottom: 10px;
            color: #555;
        }
        
        .content p {
            margin-bottom: 15px;
            line-height: 1.8;
            text-align: justify;
        }
        
        .content ul, .content ol {
            margin-left: 30px;
            margin-bottom: 15px;
        }
        
        .content li {
            margin-bottom: 5px;
        }
        
        .content code {
            background: #f4f4f4;
            padding: 2px 6px;
            border-radius: 3px;
            font-family: 'Courier New', monospace;
            font-size: 14px;
        }
        
        .content pre {
            background: #2c3e50;
            color: #ecf0f1;
            padding: 15px;
            border-radius: 5px;
            overflow-x: auto;
            margin-bottom: 15px;
        }
        
        .content blockquote {
            border-left: 4px solid #3498db;
            padding-left: 20px;
            margin: 20px 0;
            color: #666;
            font-style: italic;
            background: #f9f9f9;
            padding: 15px 20px;
        }
        
        /* 右侧批注栏 */
        .sidebar-right {
            width: 300px;
            padding: 30px 20px;
            background: #fffef5;
            border-left: 1px solid #e0e0e0;
        }
        
        .notes-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #2c3e50;
            padding-bottom: 10px;
            border-bottom: 2px solid #f39c12;
        }
        
        .note-item {
            background: white;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            border-left: 3px solid #f39c12;
        }
        
        .note-ref {
            font-size: 12px;
            color: #7f8c8d;
            margin-bottom: 5px;
        }
        
        .note-content {
            font-size: 14px;
            line-height: 1.6;
        }
        
        .note-textarea {
            width: 100%;
            min-height: 100px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            resize: vertical;
            font-family: inherit;
            font-size: 14px;
            margin-top: 10px;
        }
        
        .add-note-btn {
            background: #f39c12;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
            margin-top: 10px;
            transition: background 0.3s ease;
        }
        
        .add-note-btn:hover {
            background: #e67e22;
        }
        
        /* 响应式设计 */
        @media (max-width: 1200px) {
            .sidebar-right {
                display: none;
            }
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .sidebar-left {
                width: 100%;
                height: auto;
                position: relative;
                border-right: none;
                border-bottom: 1px solid #e0e0e0;
            }
            
            .content {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 左侧目录 -->
        <aside class="sidebar-left">
            <h2 class="toc-title">📚 目录</h2>
            <ul class="toc-list">
                <li><a href="#intro" class="toc-h1">1. 引言</a></li>
                <li><a href="#background" class="toc-h2">1.1 背景介绍</a></li>
                <li><a href="#purpose" class="toc-h2">1.2 目的与意义</a></li>
                <li><a href="#main" class="toc-h1">2. 主要内容</a></li>
                <li><a href="#theory" class="toc-h2">2.1 理论基础</a></li>
                <li><a href="#method" class="toc-h2">2.2 研究方法</a></li>
                <li><a href="#experiment" class="toc-h3">2.2.1 实验设计</a></li>
                <li><a href="#data" class="toc-h3">2.2.2 数据分析</a></li>
                <li><a href="#results" class="toc-h1">3. 结果与讨论</a></li>
                <li><a href="#conclusion" class="toc-h1">4. 结论</a></li>
            </ul>
        </aside>
        
        <!-- 中间内容区 -->
        <main class="content">
            <h1>文档标题</h1>
            
            <h2 id="intro">1. 引言</h2>
            <p>这是一个三列布局的文档模板。左侧显示目录导航，中间是主要内容区域，右侧用于添加批注和注释。这种布局方式特别适合学术文档、技术文档或需要详细注解的内容。</p>
            
            <h3 id="background">1.1 背景介绍</h3>
            <p>在现代文档编写中，清晰的结构和便捷的导航对于提高阅读体验至关重要。传统的单列文档虽然简单，但在处理复杂内容时往往显得力不从心。</p>
            
            <blockquote>
                "好的文档结构能够帮助读者快速定位所需信息，提高阅读效率。"
            </blockquote>
            
            <h3 id="purpose">1.2 目的与意义</h3>
            <p>本模板的设计目的是为了：</p>
            <ul>
                <li>提供清晰的内容层次结构</li>
                <li>方便读者快速导航</li>
                <li>支持实时批注和笔记</li>
                <li>优化阅读体验</li>
            </ul>
            
            <h2 id="main">2. 主要内容</h2>
            <p>文档的主体部分应该包含详细的论述和说明。可以使用各种 Markdown 元素来丰富内容表现：</p>
            
            <h3 id="theory">2.1 理论基础</h3>
            <p>在这里可以详细阐述理论依据。例如，我们可以使用 <code>行内代码</code> 来标记专业术语，或者使用代码块来展示示例：</p>
            
            <pre><code>// 示例代码
function example() {
    console.log("这是一个代码示例");
    return true;
}</code></pre>
            
            <h3 id="method">2.2 研究方法</h3>
            <p>研究方法部分应该详细说明采用的方法论和具体步骤。</p>
            
            <h4 id="experiment">2.2.1 实验设计</h4>
            <p>实验设计需要考虑多个因素，包括变量控制、样本选择、数据收集等。正确的实验设计是获得可靠结果的基础。</p>
            
            <h4 id="data">2.2.2 数据分析</h4>
            <p>数据分析方法的选择应该基于研究目的和数据特征。常用的分析方法包括：</p>
            <ol>
                <li>描述性统计分析</li>
                <li>推断性统计分析</li>
                <li>相关性分析</li>
                <li>回归分析</li>
            </ol>
            
            <h2 id="results">3. 结果与讨论</h2>
            <p>在这一部分，我们将展示研究结果并进行深入讨论。结果的呈现应该清晰、客观，讨论部分则需要结合理论背景进行分析。</p>
            
            <p>重要的发现可以通过特殊格式进行强调，例如使用<strong>加粗文本</strong>或者<em>斜体文本</em>。</p>
            
            <h2 id="conclusion">4. 结论</h2>
            <p>结论部分应该简明扼要地总结研究的主要发现和贡献。同时，也可以指出研究的局限性和未来的研究方向。</p>
            
            <p>这个模板提供了一个基础框架，您可以根据具体需求进行修改和扩展。右侧的批注区域可以用来添加补充说明、引用来源或者个人见解。</p>
        </main>
        
        <!-- 右侧批注栏 -->
        <aside class="sidebar-right">
            <h2 class="notes-title">📝 批注</h2>
            
            <div class="note-item">
                <div class="note-ref">关于：引言</div>
                <div class="note-content">这里可以添加对引言部分的批注，例如补充背景信息或相关引用。</div>
            </div>
            
            <div class="note-item">
                <div class="note-ref">关于：理论基础</div>
                <div class="note-content">可以在这里添加参考文献或扩展阅读材料的链接。</div>
            </div>
            
            <div class="note-item">
                <div class="note-ref">关于：数据分析</div>
                <div class="note-content">补充说明：实际应用中可能需要根据数据特点选择合适的统计方法。</div>
            </div>
            
            <!-- 添加新批注 -->
            <div style="margin-top: 30px; padding-top: 20px; border-top: 1px solid #ddd;">
                <h3 style="font-size: 16px; margin-bottom: 10px;">添加新批注</h3>
                <textarea class="note-textarea" placeholder="在这里输入您的批注..."></textarea>
                <button class="add-note-btn" onclick="alert('批注功能需要JavaScript实现')">添加批注</button>
            </div>
        </aside>
    </div>
    
    <script>
        // 平滑滚动到锚点
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
        
        // 高亮当前查看的章节
        window.addEventListener('scroll', () => {
            const sections = document.querySelectorAll('h2[id], h3[id]');
            const scrollPosition = window.scrollY + 100;
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.offsetHeight;
                const sectionId = section.getAttribute('id');
                
                if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                    document.querySelectorAll('.toc-list a').forEach(link => {
                        link.style.background = '';
                        link.style.color = '';
                    });
                    
                    const activeLink = document.querySelector(`.toc-list a[href="#${sectionId}"]`);
                    if (activeLink) {
                        activeLink.style.background = '#e8f4fd';
                        activeLink.style.color = '#3498db';
                    }
                }
            });
        });
    </script>
</body>
</html>
