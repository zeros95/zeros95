
# 这是我的博客，用于记录我的生活、学习的点点滴滴。

![头像](/images/photo.png)

---

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
   date: 2026-06-17 08:36:24
   categories: 分类
   tags: [标签1, 标签2]
   ---

   正文...
 
3. 推送：
   ```bash
   # 阅读版：
   # 1. 先查看改了哪些文件
   git status
   git diff --stat

   # 2. 暂存改动（根据情况选择）
   #    - 全部改动（新增+修改+删除）：git add -A
   #    - 仅当前目录的修改（不处理上级）：git add .
   #    - 仅指定文件：git add 文件名.md
   git add -A

   # 3. 提交
   git commit -m "类型: 改动描述"

   # 4. 推送（如被拒绝，先 pull --rebase）
   git push
   # 若报错：git pull --rebase && git push
   ```
