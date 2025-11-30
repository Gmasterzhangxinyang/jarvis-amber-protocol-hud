<p align="center"> <img src="./assets/banner.jpeg" alt="JARVIS Amber Protocol HUD Banner" width="80%"> </p> <p align="center"> <strong>⚡ A Futuristic Browser HUD Inspired by Iron Man's JARVIS</strong><br> <sub>Gesture + Voice Control + Satellite Map + Hand Tracking + AI Agent</sub> </p>
JARVIS Amber Protocol HUD (Mk. XXII)

一个基于浏览器实现的钢铁侠 JARVIS 风格 HUD，可接入 AI Agent（Dify 工作流）。

📦 Versions | 项目版本

本项目包含 两个独立可运行版本：

1. jarvis-starter（基础版）

纯前端 HUD 功能版本：

摄像头 HUD

手势识别（MediaPipe）

卫星地图导航（Leaflet + Esri）

英文语音指令（Web Speech API）

天气扫描（Open-Meteo）

文件位置：

/jarvis-starter/index.html

2. jarvis agent（AI Agent 版本）

基于 Dify 工作流扩展的智能 JARVIS。

功能包含：

聊天式回应（英文语音回复）

可接入知识库 / 工具调用 / Workflow

具备真正语义理解能力

HUD 中实时朗读 Agent 回复内容

文件位置：

/jarvis agent/jarvis-agent.html

📌 该版本附带一个工作流导出文件：
/jarvis agent/Jarvis.yml


你可以将该 Jarvis.yml 上传到 Dify，即可一键创建完整工作流。

🔊 关于语音回复（重要）

目前 JARVIS Agent 模式的语音输出 仅支持英文语音合成（TTS）
因为：

Web Speech Synthesis API 的中文声音支持度不佳

英文语音质量更自然、未来感更强

后续将在 Roadmap 中加入 Google TTS / Azure TTS 支持中文

🚀 How to Run（本地运行）

浏览器要求 HTTPS 或 localhost 才能访问摄像头 / 麦克风。

python3 -m http.server 8000


访问：

http://localhost:8000

🤖 Dify Agent Integration 教程
📌 1. 导入工作流

进入 Dify → 工作流 → 导入 → 选择：

/jarvis agent/Jarvis.yml


导入后会自动生成：

输入节点

LLM 处理节点

输出 JSON（给 HTML 使用）

📌 2. 在 HTML 内填写 API Key

打开：

/jarvis agent/jarvis-agent.html


找到以下模板并填写：

const DIFY_API_URL = "https://api.dify.ai/v1/workflows/你的流程ID/execute";
const DIFY_API_KEY = "你的API Key";

📌 3. 工作流返回的数据示例

工作流应返回结构：

{
  "reply": "Certainly sir, the weather today is sunny with 22 degrees."
}


系统将自动：

展示 HUD reply

使用英文 TTS 播放语音

恢复自动监听

🧩 Project Structure 项目结构
jarvis/
│
├── jarvis-starter/
│   └── index.html
│
├── jarvis agent/
│   ├── jarvis-agent.html
│   └── Jarvis.yml            ← Dify 工作流文件（可直接导入）
│
├── assets/
│   ├── banner.jpeg
│   ├── css/
│   ├── js/
│   └── sounds/
│
└── README.md

🛠 Roadmap（计划）
✔ 已实现：

HUD 摄像头增强

手势控制（缩放/拖拽）

卫星地图飞行动画

英文语音指令

HUD AI Agent 回答（英文语音）

🔜 即将更新：

中文语音支持（ASR + TTS）

HUD 物体识别框（YOLO）

AI 视觉问答（多模态）

AR 眼镜适配

Jetson / Edge 部署优化

👤 作者

Created by Bobby
GitHub: https://github.com/Gmasterzhangxinyang

欢迎 PR / 合作。
