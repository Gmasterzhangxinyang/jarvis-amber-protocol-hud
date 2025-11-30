<p align="center">
  <img src="./assets/banner.jpeg" alt="JARVIS Amber Protocol HUD Banner" width="80%">
</p>

<p align="center">
  <strong>⚡ A Futuristic Browser HUD Inspired by Iron Man's JARVIS</strong><br>
  <sub>Gesture + Voice Control + Satellite Map + Hand Tracking + AI Agent</sub>
</p>

---

# JARVIS Amber Protocol HUD (Mk. XXII)
一个基于浏览器实现的钢铁侠 JARVIS 琥珀协议 HUD，可扩展语音、手势、地图、天气与 AI 智能助手。

---

# 📦 项目版本说明 | Versions

本项目包含 **两个可运行版本**：分别用于展示 HUD 效果与接入 AI 功能。

---

## 1. jarvis-starter（基础 HUD 版本）

纯前端 HUD 功能，包括：

- 实时摄像头 HUD（Amber 风格滤镜）
- 手势识别（MediaPipe Hands）
- 卫星地图导航（Leaflet + Esri 全球影像）
- 基础语音指令（英文）
- 天气扫描（Open-Meteo）

**入口文件：**

```
/jarvis-starter/index.html
```

---

## 2. jarvis agent（AI Agent 版本）

增强版 JARVIS，可连接 **Dify 工作流** 实现 AI 对话能力。

新增能力：

- LLM AI 对话（像真正的 JARVIS 回应你）
- 自动语音朗读（当前仅支持英文 TTS）
- 支持 Dify 工作流导入
- 可执行复杂任务 / 查询天气 / 回答问题

**关键文件：**

```
/jarvis agent/jarvis-agent.html
/jarvis agent/Jarvis.yml
```

---

# 🔊 语音说明（重要）

- **当前版本仅支持英文语音回复（TTS）**
- 中文 TTS 版本将在未来更新加入

---

# 🤖 如何绑定 Dify 工作流（AI Agent）

## ① 导入工作流

在 Dify：

```
工作流 → 导入 → 选择 /jarvis agent/Jarvis.yml
```

自动生成：

- 文本输入节点（语音识别结果）
- LLM 推理节点
- JSON 输出节点

---

## ② 配置 API

打开：

```
/jarvis agent/jarvis-agent.html
```

搜索：

```js
const DIFY_API_URL
const DIFY_API_KEY
```

填入你自己的 API 信息：

```js
const DIFY_API_URL = "https://api.dify.ai/v1/workflows/<你的流程ID>/execute";
const DIFY_API_KEY = "<你的Key>";
```

---

## ③ 工作流返回 JSON

AI 最终响应需返回：

```json
{
  "reply": "Sir, the system is now online and fully operational."
}
```

HUD 自动：

- 显示文字  
- 用英文朗读  
- 恢复自动监听  

---

# 🚀 本地运行方式（需要 localhost）

```bash
cd project-folder
python3 -m http.server 8000
```

访问：

```
http://localhost:8000
```

---

# 🧩 项目结构

```
jarvis/
│
├── jarvis-starter/
│   └── index.html
│
├── jarvis agent/
│   ├── jarvis-agent.html
│   └── Jarvis.yml
│
├── assets/
│   ├── banner.jpeg
│
└── README.md
```

---

# 🛠 Roadmap | 后续计划

- 中文语音识别 / 中文 TTS  
- YOLO 目标检测 HUD  
- 多模态视觉问答  
- Jetson / AR 眼镜适配  
- 更多电影级 HUD 动画  

---

# 👤 作者

Created by **Bobby**  
GitHub: https://github.com/Gmasterzhangxinyang

欢迎 PR、合作、扩展。
