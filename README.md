# 🌐 语跃 LinguaLeap

> 一门外语，一次跃迁。—— 沉浸式多语种在线学习平台（英语 / 日语 / 韩语）

🔗 **在线体验**：[https://clyde-ux.github.io/lingauleap/](https://clyde-ux.github.io/lingauleap/)

---

## ✨ 功能特性

### 1. 分级课程体系
- 🇬🇧 英语：A1 入门 → A2 基础 → B1 进阶
- 🇯🇵 日语：N5 → N4 → N3
- 🇰🇷 韩语：TOPIK Ⅰ → TOPIK Ⅱ → TOPIK Ⅲ
- 每节课包含单词、语法、口语、听力四大环节，形成完整学习闭环

### 2. 四大互动学习模块
| 模块 | 能力 |
|---|---|
| 🃏 单词记忆 | 3D 翻转闪卡，认识 / 模糊 / 不认识三档反馈，生词自动进入间隔重复复习队列 |
| ✍️ 语法练习 | 知识点讲解 → 即学即练 → 逐题解析 |
| 🎤 口语跟读 | 基于 Web Speech API 的语音识别 + 相似度算法发音评分，支持慢速示范；浏览器不支持时自动降级为自评模式 |
| 🎧 听力训练 | TTS 真人语速朗读 + 0.55x 慢速重播 + 听后理解选择题 |

### 3. 学习进度追踪
- 近 14 天 XP 学习曲线（纯 SVG 手绘图表）
- 28 天打卡热力图
- 四大模块正确率分析、各语言进度、等级进度环

### 4. 用户体系
- 邮箱注册 / 登录、会话保持、头像昵称与学习语言偏好设置
- 内置**演示账号**（含预置学习数据）与**游客快速体验**

### 5. 个性化学习路径
- 6 题定级测试，自动推荐起点级别
- 推荐引擎综合「到期复习 + 薄弱模块强化 + 下一课继续 + 连续打卡提醒」生成每日任务
- 可视化学习路线图，完成进度一目了然

### 6. 社区与成就激励
- 学习社区：发帖（5 类话题标签）、点赞、评论
- 成就殿堂：13 枚徽章条件解锁，解锁即时弹窗庆祝
- XP 等级体系 + 学霸排行榜

---

## 🛠 技术实现

- **零依赖单文件**：全部功能封装于一个 `index.html`（HTML + CSS + 原生 JavaScript），无需构建、无框架、无外部 CDN
- **语音能力**：`SpeechSynthesis`（TTS 朗读）+ `SpeechRecognition`（跟读识别），多语言语音（en-US / ja-JP / ko-KR）
- **数据持久化**：`localStorage`，注册用户、学习进度、复习计划、社区帖子本地保存
- **发音评分**：编辑距离（Levenshtein）字符相似度算法
- **图表**：手写 SVG 折线图、环形进度、CSS 热力图，无图表库依赖

## 🚀 快速开始

**方式一：在线直接使用**
打开 [https://clyde-ux.github.io/lingauleap/](https://clyde-ux.github.io/lingauleap/) 即可，推荐使用 Chrome 浏览器（语音评分功能完整）。

**方式二：本地运行**

```bash
git clone https://github.com/clyde-ux/lingauleap.git
cd lingauleap
# 直接双击 index.html 打开，或启动本地服务：
python3 -m http.server 8080
# 访问 http://localhost:8080
```

**演示账号**：`demo@lingualeap.cn` / `demo123`（含预置的 520 XP、连续打卡、课程进度与复习队列数据，便于快速体验全部功能）

## 📁 项目结构

```
lingauleap/
├── index.html   # 平台全部代码（页面结构 / 样式 / 逻辑 / 课程数据）
└── README.md
```

## 📌 说明

- 本项目为前端演示项目，所有数据存储于浏览器本地，不会上传至任何服务器
- 口语跟读需要 HTTPS 环境与麦克风权限；在不支持的浏览器中将自动切换为自评模式
- 欢迎通过 Issue / PR 反馈问题与建议

## 📄 License

[MIT](https://opensource.org/licenses/MIT) © 2026 clyde-ux
