---
layout: page
title: Blog
permalink: /blog/
---

<style>
  .blog-container {
    display: flex;
    gap: 2rem;
    position: relative;
  }
  
  .toc-sidebar {
    flex: 0 0 250px;
    position: sticky;
    top: 20px;
    height: fit-content;
    max-height: calc(100vh - 40px);
    overflow-y: auto;
    padding: 1rem;
    background: #f5f5f5;
    border-radius: 8px;
  }
  
  .toc-sidebar h2 {
    font-size: 1rem;
    margin-bottom: 1rem;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid #333;
  }
  
  .toc-sidebar ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .toc-sidebar li {
    margin-bottom: 0.5rem;
  }
  
  .toc-sidebar a {
    color: #333;
    text-decoration: none;
    display: block;
    padding: 0.25rem 0.5rem;
    border-radius: 4px;
    transition: background 0.3s;
  }
  
  .toc-sidebar a:hover {
    background: #e0e0e0;
  }
  
  .toc-sidebar .toc-active {
    background: #007bff;
    color: white;
  }
  
  .toc-sidebar ul ul {
    margin-left: 1rem;
    margin-top: 0.25rem;
  }
  
  .blog-content {
    flex: 1;
    min-width: 0;
  }
  
  @media (max-width: 768px) {
    .blog-container {
      flex-direction: column;
    }
    
    .toc-sidebar {
      position: relative;
      top: 0;
      max-height: none;
      margin-bottom: 2rem;
    }
  }
</style>

<div class="blog-container">
  <nav class="toc-sidebar">
    <h2>📑 Table of Contents</h2>
    <ul>
      <li><a href="#about-blog">关于本博客</a></li>
      <li>
        <a href="#technical-articles">技术文章</a>
        <ul>
          <li><a href="#frontend-dev">前端开发</a></li>
          <li><a href="#backend-tech">后端技术</a></li>
          <li><a href="#database">数据库</a></li>
        </ul>
      </li>
      <li>
        <a href="#learning-notes">学习笔记</a>
        <ul>
          <li><a href="#javascript">JavaScript进阶</a></li>
          <li><a href="#python">Python实战</a></li>
        </ul>
      </li>
      <li><a href="#projects">项目展示</a></li>
      <li><a href="#resources">资源分享</a></li>
      <li><a href="#contact">联系方式</a></li>
    </ul>
  </nav>
  
  <div class="blog-content">

## 关于本博客 {#about-blog}

欢迎来到我的技术博客！这里记录了我的学习历程和技术心得。我主要关注Web开发、云计算和人工智能等领域。

本博客会定期更新，分享实用的技术文章和项目经验。

---

## 技术文章 {#technical-articles}

### 前端开发 {#frontend-dev}

前端开发是构建用户界面的艺术。在这个部分，我会分享关于HTML5、CSS3、JavaScript以及各种前端框架的使用经验。

**最新文章：**
- React Hooks深入理解与实践
- Vue 3 Composition API完全指南
- 现代CSS布局技巧总结
- TypeScript类型体操实战

### 后端技术 {#backend-tech}

后端开发是应用程序的核心。这里包含了关于Node.js、Python、Java等后端技术栈的文章。

**热门内容：**
- RESTful API设计最佳实践
- 微服务架构入门指南
- Docker容器化部署实战
- Kubernetes集群管理

### 数据库 {#database}

数据库是应用的基石。本节涵盖关系型数据库和NoSQL数据库的设计与优化。

**推荐阅读：**
- MySQL性能优化技巧
- MongoDB聚合管道详解
- Redis缓存策略实践

---

## 学习笔记 {#learning-notes}

### JavaScript进阶 {#javascript}

JavaScript是前端开发的核心语言。这里记录了我学习JS高级特性的笔记。

**核心主题：**
- 闭包与作用域链
- 原型链与继承
- 异步编程模式
- ES6+新特性总结

### Python实战 {#python}

Python在数据科学、Web开发、自动化等领域都有广泛应用。

**实战项目：**
- Web爬虫开发实战
- Django REST框架应用
- 数据分析与可视化
- 机器学习入门项目

---

## 项目展示 {#projects}

以下是我参与或独立完成的一些开源项目：

| 项目名称 | 技术栈 | 描述 | 链接 |
|---------|--------|------|------|
| TodoApp | React + Node.js | 全栈待办事项应用 | [GitHub](https://github.com) |
| DataViz | D3.js + Python | 数据可视化平台 | [Demo](https://example.com) |
| ChatBot | Python + NLP | 智能聊天机器人 | [文档](https://docs.com) |

---

## 资源分享 {#resources}

### 📚 推荐书籍
- 《JavaScript高级程序设计》
- 《深入理解计算机系统》
- 《设计模式：可复用面向对象软件的基础》

### 🔧 开发工具
- **编辑器**: VS Code, WebStorm
- **版本控制**: Git, GitHub
- **调试工具**: Chrome DevTools
- **API测试**: Postman, Insomnia

### 🌐 学习网站
- [MDN Web Docs](https://developer.mozilla.org)
- [Stack Overflow](https://stackoverflow.com)
- [GitHub](https://github.com)
- [LeetCode](https://leetcode.com)

---

## 联系方式 {#contact}

如果你有任何问题或建议，欢迎通过以下方式联系我：

- 📧 Email: example@email.com
- 💼 LinkedIn: [我的LinkedIn](https://linkedin.com)
- 🐙 GitHub: [@username](https://github.com)
- 🐦 Twitter: [@username](https://twitter.com)

  </div>
</div>

<script>
  // 高亮当前章节
  function highlightTOC() {
    const sections = document.querySelectorAll('.blog-content h2, .blog-content h3');
    const tocLinks = document.querySelectorAll('.toc-sidebar a');
    
    const scrollPosition = window.scrollY + 100;
    
    sections.forEach((section, index) => {
      const sectionTop = section.offsetTop;
      const sectionHeight = section.offsetHeight;
      const sectionId = section.id;
      
      if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
        tocLinks.forEach(link => {
          link.classList.remove('toc-active');
          if (link.getAttribute('href') === '#' + sectionId) {
            link.classList.add('toc-active');
          }
        });
      }
    });
  }
  
  // 平滑滚动
  document.querySelectorAll('.toc-sidebar a').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
      e.preventDefault();
      const targetId = this.getAttribute('href').substring(1);
      const targetSection = document.getElementById(targetId);
      if (targetSection) {
        window.scrollTo({
          top: targetSection.offsetTop - 20,
          behavior: 'smooth'
        });
      }
    });
  });
  
  // 监听滚动
  window.addEventListener('scroll', highlightTOC);
  highlightTOC();
</script>
