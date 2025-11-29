<p align="center">
  <img src="./banner.jpeg" width="90%" style="border-radius:12px;" />
</p>

<p align="center">
  <b>⚡ A Futuristic Browser HUD Inspired by Iron Man's JARVIS</b>
</p>



# JARVIS Amber Protocol HUD (Mk. XXII)
A browser-based futuristic HUD inspired by Iron Man’s JARVIS system.
一个基于浏览器实现的钢铁侠 JARVIS 风格 HUD 系统（Mk. XXII 琥珀协议）。

---

## ✨ Features | 功能特性

### Real-time HUD Camera Overlay
- Live camera with holographic amber filter
- 实时摄像头画面 + 琥珀色全息视觉效果

### Hand Tracking (MediaPipe Hands)
- Gesture skeleton rendering
- Pinch to drag map
- Open-hand to zoom
- 手势骨架渲染、捏合拖拽、张手缩放

### Voice Commands (Web Speech API)
- Continuous auto-listening
- 支持自动循环语音识别

Available commands 包含指令：
- open / close map（打开/关闭地图）
- full screen / minimize（全屏/退出全屏）
- zoom in / zoom out（放大/缩小）
- go to *city*（跳转城市）
- detailed image（真彩模式）
- check weather（查询天气）

### Satellite Map (Leaflet + Esri)
- Global satellite imagery
- Smooth fly-to navigation
- 全球卫星视图、飞行动画、语音导航

### Weather Scan (Open-Meteo)
- Current temperature & weather
- 实时温度与天气状况扫描

---


## 🚀 How to Run | 本地运行方式

Browsers require HTTPS or localhost for camera/mic.
浏览器要求通过 HTTPS 或 localhost 才能访问摄像头和麦克风。

### Recommended (Python)
```bash
cd project-folder
python3 -m http.server 8000
```

Visit / 访问：
```
http://localhost:8000
```

---

## 🛠 Future Roadmap | 后续开发计划

### 1. AI Agent Integration | AI 智能助手接入
- Support Gemini / GPT / 本地模型
- Provide conversational JARVIS assistant
- 支持低代码平台例如Dify，Coze接入
- 支持任意问题、场景理解、多模态推理

### 2. Object Detection HUD | 物体识别 HUD
- Real-time detection boxes and labels
- 实时目标识别并显示 HUD 标注框

### 3. Hardware Support | 硬件适配
- Jetson / Raspberry Pi
- AR glasses / HUD devices
- 支持 AR 眼镜、嵌入式设备部署

### 4. Multi-language Voice | 多语言语音
- Chinese voice commands
- 中文语音识别支持

### 5. UI Enhancements | 界面增强
- More cinematic HUD animations
- 更多 JARVIS 风格动画与组件

欢迎贡献（Issues / PR）。

---

## 📄 License | 许可证

MIT License  
自由使用、修改、分发，需保留版权声明。

---

## 👤 Author | 作者

Created by Bobby  
由 Bobby 开发  
GitHub: https://github.com/Gmasterzhangxinyang

欢迎一起改进与扩展这个 JARVIS HUD 项目。
