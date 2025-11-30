<p align="center"> <img src="./assets/banner.jpeg" alt="JARVIS Amber Protocol HUD Banner" width="80%"> </p> <p align="center"> <strong>⚡ A Futuristic Browser HUD Inspired by Iron Man's JARVIS</strong><br> <sub>Gesture + Voice Control + Satellite Map + Hand Tracking + AI Agent</sub> </p>
JARVIS Amber Protocol HUD (Mk. XXII)

📦 项目版本说明 | Versions

本项目包含 两个可运行版本：用于不同场景和扩展能力。

1. jarvis-starter（基础 HUD 版本）

纯前端 HUD 功能，包括：

实时摄像头 HUD（Amber 风格滤镜）📦 项目版本说明 | Versions

本项目包含 两个可运行版本：用于不同场景和扩展能力。

1. jarvis-starter（基础 HUD 版本）

纯前端 HUD 功能，包括：

实时摄像头 HUD（Amber 风格滤镜）

适合 想看 HUD 效果、手势控制、地图导航 的用户。

2. jarvis agent（AI Agent 版本）

可接入 Dify 工作流、LLM、知识库、工具调用 的 JARVIS 增强版。

新增能力：

AI 对话能力（HUD 中可听见回复）

连接 Dify 工作流（Jarvis.yml）

能回答任意问题、执行任务

自动 TTS 语音朗读（英文）

入口文件：

/jarvis agent/jarvis-agent.html


📌 该目录包含一个配置文件，可直接导入 Dify：

/jarvis agent/Jarvis.yml


导入即可自动创建工作流。

🔊 语音说明（重要）
当前版本语音回复仅支持英文 TTS

原因：

Web Speech Synthesis API 的中文发音支持度不稳定

英文 AI 声音更自然、更有 JARVIS 科幻感

后续将加入 Google TTS / Azure TTS 以支持中文

🤖 如何接入 Dify 工作流（AI Agent 模式）
1. 导入工作流

进入 Dify：

工作流 → 导入 → 选择 /jarvis agent/Jarvis.yml


系统会自动生成：

语音文本输入

LLM 处理节点

JSON 输出节点

2. 在 HTML 中配置 Dify API

打开：

/jarvis agent/jarvis-agent.html


找到以下内容：

const DIFY_API_URL = "https://api.dify.ai/v1/workflows/你的流程ID/execute";
const DIFY_API_KEY = "你的API Key";


填写你自己的信息即可。

3. 工作流需返回 JSON

示例：

{
  "reply": "Sir, the weather today is sunny with a temperature of 22 degrees."
}


前端会自动：

显示 HUD 回应文字

英文语音朗读

恢复自动监听

🚀 本地运行方式（HTTPS/localhost）

浏览器要求 localhost/HTTPS 才能访问摄像头与麦克风。

推荐方式：

cd project-folder
python3 -m http.server 8000


访问：

http://localhost:8000

🧩 项目结构（Project Structure）
jarvis/
│
├── jarvis-starter/
│   └── index.html
│
├── jarvis agent/
│   ├── jarvis-agent.html
│   └── Jarvis.yml     ← Dify 工作流配置文件
│
├── assets/
│   ├── banner.jpeg
│   ├── css/
│   ├── js/
│   └── sounds/
│
└── README.md

🛠 Roadmap | 后续计划
✔ 已完成

HUD 摄像头增强

手势控制

卫星地图导航

天气扫描

英文语音识别

Dify AI Agent 接入（英文 TTS）

🔜 即将更新

中文语音识别 & TTS

YOLO HUD 物体识别框

多模态视觉问答

Jetson / AR 眼镜适配

UI HUD 动画增强

👤 作者

Created by Bobby
GitHub: https://github.com/Gmasterzhangxinyang

欢迎 PR、合作、扩展。
