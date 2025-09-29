# 纯 README.md 方案（使用表格布局）

## 方案1：使用表格实现左右布局

```markdown
# Songtao Liu's Blog

<table>
<tr>
<td valign="top" width="25%">

## 📑 Navigation

- [🏠 Home](#home)
- [👨‍💻 About Me](#about-me)
- [📝 Blog Posts](#blog-posts)
  - [Frontend](#frontend-development)
  - [Backend](#backend-technology)
  - [Database](#database-design)
- [📚 Notes](#learning-notes)
  - [JavaScript](#javascript-advanced)
  - [Python](#python-practice)
- [🚀 Projects](#projects)
- [📦 Resources](#resources)
- [📫 Contact](#contact)

</td>
<td valign="top" width="75%">

## Home

Welcome to my technical blog! Here I share my learning journey and technical insights.

## About Me

I'm a full-stack developer passionate about web development, cloud computing, and artificial intelligence. I enjoy building innovative solutions and sharing knowledge with the community.

## Blog Posts

### Frontend Development

#### Recent Articles
- **React Hooks Deep Dive** - Understanding useState, useEffect and custom hooks
- **Vue 3 Composition API** - Complete guide with practical examples
- **Modern CSS Layout** - Grid, Flexbox, and Container Queries
- **TypeScript Best Practices** - Type safety in large applications

### Backend Technology

#### Popular Topics
- **RESTful API Design** - Best practices and patterns
- **Microservices Architecture** - Building scalable systems
- **Docker Deployment** - Containerization strategies
- **Node.js Performance** - Optimization techniques

### Database Design

#### Featured Content
- **MySQL Optimization** - Query performance tuning
- **MongoDB Aggregation** - Pipeline operations explained
- **Redis Caching** - Implementation strategies
- **PostgreSQL vs MySQL** - Choosing the right database

## Learning Notes

### JavaScript Advanced

Core concepts I've been studying:
- Closures and Scope Chain
- Prototypal Inheritance
- Asynchronous Programming (Promises, Async/Await)
- ES6+ Features
- Functional Programming Paradigms

### Python Practice

Real-world applications:
- Web Scraping with BeautifulSoup
- Django REST Framework
- Data Analysis with Pandas
- Machine Learning with Scikit-learn
- Automation Scripts

## Projects

| Project | Tech Stack | Description | Links |
|---------|-----------|-------------|-------|
| TodoApp | React + Node.js | Full-stack task manager | [GitHub](https://github.com) · [Demo](https://demo.com) |
| DataViz | D3.js + Python | Data visualization platform | [GitHub](https://github.com) · [Live](https://live.com) |
| ChatBot | Python + NLP | AI-powered chatbot | [Docs](https://docs.com) · [API](https://api.com) |
| E-Commerce | Vue + Spring | Online shopping platform | [GitHub](https://github.com) |

## Resources

### 📚 Books
- JavaScript: The Good Parts
- Clean Code
- Design Patterns
- The Pragmatic Programmer

### 🛠 Tools
- **Editor**: VS Code
- **Version Control**: Git
- **API Testing**: Postman
- **Containerization**: Docker

### 🌐 Websites
- [MDN Web Docs](https://developer.mozilla.org)
- [Stack Overflow](https://stackoverflow.com)
- [Dev.to](https://dev.to)

## Contact

- 📧 Email: songtao.liu@example.com
- 🐙 GitHub: [@songtaoliu](https://github.com)
- 💼 LinkedIn: [Songtao Liu](https://linkedin.com)
- 🐦 Twitter: [@songtaoliu](https://twitter.com)

</td>
</tr>
</table>
```

---

## 方案2：使用折叠式目录（Collapsible TOC）

```markdown
# Songtao Liu's Blog

<details open>
<summary><b>📑 Table of Contents</b></summary>

- [About Me](#about-me)
- [Blog Posts](#blog-posts)
  - [Frontend Development](#frontend-development)
  - [Backend Technology](#backend-technology)
  - [Database Design](#database-design)
- [Learning Notes](#learning-notes)
  - [JavaScript Advanced
