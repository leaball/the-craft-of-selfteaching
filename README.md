# 📘 Leah 的the learning log of basic 操作 of progranmming

> 👩🏻‍💻 This is my personal learning tracker based on the project [the-craft-of-selfteaching](https://github.com/selfteaching/the-craft-of-selfteaching).
> 
> I am using this study branch to experiment, take notes, and build confidence with Python, Git, Jupyter, and VS Code.  
> 
> 👉 Proof of Work is important — I want to **see my own progress** in traceable steps.

---

## ✅ 2025-07-08 learning log 学习日志（Day 4）

### 🎯 Today's Goals:
- Understand the difference between "cloning a project" and manually copying files 
- Day 2 - Clarify the purpose of GitHub branches (master / study / PR branch) and warm up for Feb record - 复习 2 月进展：分支的用途
- Practice using the terminal to open Jupyter Notebook  `jupyter notebook` 
- Successfully push local changes to GitHub (token setup)（解决认证问题）
  
### 🛠️ Technical Steps:

- Switched to `study` branch using `git checkout study`
- Started Jupyter Notebook using `jupyter notebook` 启动学习文件 via terminal 
- Set up GitHub authentication with personal access token (PAT) 创建并粘贴 Personal Access Token（PAT）替代 Git 密码
  
    #### 📌 步骤如下：

    1、👉 [Sign in to GitHub · GitHub](https://github.com/settings/tokens)
    2、选择 ** “Personal access tokens (classic)”，点 “Generate new token”
        设置 token 时：
    - Note: 起名：`push from terminal`
    - Expiration: 选择 30 天或 90 天（看你希望保存多久）
    - Scope: 至少勾选：
      - `repo` ✅  
      - `workflow`（如果你想以后玩 GitHub Action）✅
      
    3、生成 token 后，复制这个长长的字串（只显示一次），然后：
        在终端执行 `git push origin study` 时，Git 会提示你输入用户名和密码：
    - **Username**: 
    - **Password**: **粘贴那个 token 字串**（⚠️ 不是 GitHub 密码） 🔒 注意：这个 token 是你“数字身份的钥匙”，别发给任何人！
    
    4、使用 `git remote set-url` 成功重设为 HTTPS Token 模式

  （而非粘贴输入 - 由于终端不显示，总是不确定是否粘贴成功）
    
    ```bash
    git remote set-url origin https://<your_token>@github.com/leaball/the-craft-of-selfteaching.git
    ```
    
    把 `<your_token>` 替换为你刚才复制的那一串 Token，这样就不用再交互输入用户名和密码了。比如：
    
    ```bash
    git remote set-url origin https://ghp_abc123xyz456789@github.com/leaball/the-craft-of-selfteaching.git
    ```
- Ran `git push origin study` to upload changes 成功上传第一次修改

### 🧠 Reflections:
- Cloned projects contain `.git` and are **version-controlled**; copies do not - clone 下来的文件包含 `.git` 是真正“带版本控制”的，复制的不行
- GitHub is like my public learning archive — pushing means I "turn in my work"
- Even if I'm still unsure about writing code, I can follow and run examples 
- Small wins like pushing a log file make learning feel real and measurable


### 💬 One thought: 
> "I may not solve coding problems yet, but I dare to face my fears and learn the tools. That itself is proof of work."


### ✅ 2025-07-08 补充记录

我试着不用 VS Code，而是在 Jupyter 中直接创建了 Markdown 文件，并成功 push 到 study 分支！

这让我感觉：技术也没那么遥远，它只是一种表达的方式。

关键是：**我可以选择我喜欢、我能控制的路径。**


## 🧾 我的 commit 日志模版（备查）
✍️ 第二部分：commit 信息的设计与用途解释（重点来咯）

### ❓什么是 commit message？

每次保存代码的变动并提交（`git commit`）的时候，写一句**“这次我干了什么”的信息**，称为 `commit message`。

这就像写日记时标题那样，Git 会把每一次的动手行为都记录下来，并加上“标题”。

---

### 🧾 常见 commit 信息格式（标准写法）

```bash
<类型>(<范围>): <描述内容>
```

比如：

```
feat(notebook): 完成第3章列表推导式的运行和理解
```

解释如下：

| 部分  | 含义  |
| --- | --- |
| `feat` | **Feature**，做了一个新功能、新实验、新步骤 |
| `(notebook)` | 涉及的范围，比如修改的是 Jupyter notebook |
| `完成第3章列表推导式的运行和理解` | 可用中文描述这次干了什么，非常人性化 |

---

### ✅ 常见的类型分类（可参考这个来写）

| 类型标记 | 说明  | 示例  |
| --- | --- | --- |
| `feat` | 加了新练习、新运行、新思路 | `feat: 加了自己的 for loop 例子` |
| `note` | 纯笔记、理解记录 | `note: 理解了 print 的 format string 用法` |
| `test` | 做了一些测试运行 | `test: 修改了 if 条件表达式测试输入输出` |
| `fix` | 修 bug，比如代码报错你改掉了 | `fix: 解决了路径错误导致无法运行的问题` |
| `chore` | 非代码本身，比如更新 README | `chore: 更新了学习日志` |
| `refactor` | 重构，优化代码结构（目前你可以不常用） |     |

---

### 🧪 example
```bash
git add .
git commit -m "feat(notebook): 跑通了前两章的运行例子并添加中文注释"
git push origin study
```

如果只是做了小调整、打了一些注释，也可以这样写：

```bash
git commit -m "note(reflection): 在 entrance 章节笔记里加入了学习理解"
```

