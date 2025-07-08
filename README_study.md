# 📘 Lea 的技术成长记录（study 分支）

> 👩🏻‍💻 This is my personal learning tracker based on the project [the-craft-of-selfteaching](https://github.com/selfteaching/the-craft-of-selfteaching).
> 
> I am using this study branch to experiment, take notes, and build confidence with Python, Git, Jupyter, and VS Code.  
> 
> 👉 Proof of Work is important — I want to **see my own progress** in traceable steps.

---

## ✅ 2025-07-08 学习日志（Day 4）

#### 🎯 今日目标：
- 弄清楚 clone 下来的项目和复制文件的区别
- 继续 Day2 - 分清了 GitHub 分支（master / study / PR 分支）的用途
- 学习 Terminal 命令操作，成功打开 Jupyter Notebook
- 成功 push 本地更改到 GitHub（解决认证问题）

#### 🛠️ 技术操作：
- `git checkout study` 切换分支
- `jupyter notebook` 启动学习文件
- 创建并粘贴 Personal Access Token（PAT）替代 Git 密码 -
#### 📌 步骤如下：1、👉 [Sign in to GitHub · GitHub](https://github.com/settings/tokens)
  选择 **“Fine-grained tokens” 或 “Personal access tokens (classic)”**，点 “Generate new token”
 2. 设置 token 时：
- Note: 起名：**`push from terminal`**
- Expiration: 选择 30 天或 90 天（看你希望保存多久）
- Scope: 至少勾选：
  - `repo` ✅  
  - `workflow`（如果你想以后玩 GitHub Action）✅
  
  3. 生成 token 后，复制这个长长的字串（只显示一次），然后：
    在终端执行 `git push origin study` 时，Git 会提示你输入用户名和密码：
- **Username**: 填你的 GitHub 用户名（比如 `leaball`）
- **Password**: **粘贴那个 token 字串**（⚠️ 不是 GitHub 密码）

  ** 🔒 注意：这个 token 是你“数字身份的钥匙”，别发给任何人！**

4、使用 `git remote set-url` 成功重设为 HTTPS Token 模式
    可以试试这个替代方法：

```bash
git remote set-url origin https://<your_token>@github.com/leaball/the-craft-of-selfteaching.git
```

把 `<your_token>` 替换为你刚才复制的那一串 Token，这样就不用再交互输入用户名和密码了。比如：

```bash
git remote set-url origin https://ghp_abc123xyz456789@github.com/leaball/the-craft-of-selfteaching.git
```

然后直接运行：
- `git push origin study` 成功上传第一次修改

#### 🧠 我的理解与收获：
- clone 下来的文件包含 `.git` 是真正“带版本控制”的，复制的不行
- GitHub 是你在线的学习记录空间，push 相当于“交作业”
- 运行 notebook 虽然还卡，但整个流程能跑通，内心有踏实感
- 成功 push 的那一刻，好像真的有个“我在认真学”的证据被世界看到了

#### 💬 小记一句：
> “我虽然还不能独立写代码解决问题，但我敢面对恐惧，敢学习新的工具 —— 这就是我的 Proof of Work。”

### ✅ 2025-07-08 补充记录

我试着不用 VS Code，而是在 Jupyter 中直接创建了 Markdown 文件，并成功 push 到 study 分支！

这让我感觉：技术也没那么遥远，它只是一种表达的方式。

关键是：**我可以选择我喜欢、我能控制的路径。**

---

## 🧾 我的 commit 日志模版（备查）

```bash
# 示例 commit 信息
git commit -m "feat(init): 创建 Lea 的 study 分支学习日志 README_study.md"
