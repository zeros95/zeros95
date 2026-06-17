
# 这是我的博客，用于记录我的生活、学习的点点滴滴。

## 1、博客地址：https://morningligt.github.io

---

##  2、文件夹说明

| 文件夹/文件 | 用途 |
| :--- | :--- |
| `_posts/` | 所有文章放这里（`YYYY-MM-DD-标题.md`） |
| `images/` | 博文配图 |
| `_layouts/` | 页面布局模板（一般不用动） |
| `_config.yml` | 博客配置文件（标题、主题、导航等） |
| `index.md` | 首页 |
| `about.md` | 关于我 |
| `categories.md` | 分类页 |
| `tags.md` | 标签页 |
| `archive.md` | 归档页 |
| `standard.md` | 写作规范，比如标签、分类的枚举值 |

---

## 3、写新文章

1. 在 `_posts/` 新建 `YYYY-MM-DD-标题.md`
2. 复制这个模板：
   ```yaml
   ---
   layout: post
   title: 标题
   date: 2026-06-17
   categories: 分类
   tags: [标签1, 标签2]
   ---

   正文...
 
3. 推送：
   ```bash
   git pull
   git add .
   git commit -m "新增：标题"
   git push
   ```
