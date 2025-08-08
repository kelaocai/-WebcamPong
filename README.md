
# 🎮 Webcam Pong

> A tribute to the classic **Pong** — powered by **GPT-5** and your webcam.  
> Real-time hand tracking with bone visualization, AI-assisted paddle control, and an 80s arcade style.  
> 致敬经典 Pong，由 GPT-5 辅助生成，通过摄像头实时手势识别控制球拍，支持骨骼可视化与 AI 辅助补位，重现 80 年代街机风格。

---

## ✨ Features 功能特性

- 📷 **Webcam Hand Control / 摄像头手势控制**  
  Use TensorFlow.js Handpose to detect your hand in real time, moving your index finger up/down to control the paddle.  
  使用 TensorFlow.js Handpose 实时识别手势，通过食指上下移动控制球拍。

- 🖐 **Hand Skeleton Visualization / 手部骨骼可视化**  
  Draws hand keypoints and bone lines for clear gesture feedback.  
  实时绘制手部关键点和骨骼连线，让手势反馈更直观。

- 🖼 **9:16 Centered Crop / 9:16 人物居中裁剪**  
  Keeps the camera feed in original aspect ratio, automatically centered on your hand.  
  保持摄像头画面原始比例，自动以手部为中心进行居中裁剪。

- 🟩 **Semi-Transparent Detection Box / 绿色半透明识别框**  
  Highlights the optimal area for control.  
  提示最佳手势控制区域，提升游戏体验。

- 🎯 **Full-Height Mapping / 全高度映射**  
  Small hand movements cover the full paddle range.  
  手部小范围移动即可覆盖游戏全高度。

- 🤖 **AI Assist / AI 辅助补位**  
  Paddle auto-adjusts when the ball nears the edge.  
  当球接近边界时，自动微调球拍，防止漏球。

- 🏓 **Unlimited Score / 无上限比分**  
  Game runs endlessly with real-time scoring.  
  无上限比分，游戏可持续进行。

---

## 📸 Demo 演示

| Game Screen / 游戏界面 | Camera View / 摄像头识别 |
| --- | --- |
| ![Game](docs/game-demo.png) | ![Camera](docs/camera-demo.png) |

---

## 🛠 Tech Stack 技术栈

- **HTML5 Canvas** — Game rendering / 游戏画面绘制
- **TensorFlow.js** (`@tensorflow-models/handpose`) — Hand tracking / 手部识别
- **JavaScript** — Logic control / 前端逻辑控制
- **WebRTC** (`navigator.mediaDevices.getUserMedia`) — Webcam access / 摄像头采集
- **GPT-5 Assisted Development / GPT-5 辅助开发** — Code generation & optimization / 代码生成与优化

---

## 🚀 How to Run / 本地运行

1. **Clone the project / 克隆项目**
   ```bash
   git clone https://github.com/your-username/webcam-pong.git
   cd webcam-pong


2. **Start a local server / 启动本地服务器**
   To avoid browser webcam permission issues, run a local server:
   为避免浏览器限制摄像头权限，需要启动本地服务器：

   ```bash
   # Python 3
   python -m http.server 8000
   ```

3. **Open in browser / 打开浏览器访问**

   ```
   http://localhost:8000
   ```

4. **Allow webcam permission / 允许摄像头权限**
   Keep your hand inside the detection box and move it up/down to control the right paddle.
   将手保持在识别框内，上下移动即可控制右侧球拍。

---

## 🎮 Controls / 操作说明

* **Right Paddle / 右拍** — Controlled by webcam hand tracking
  由摄像头识别的手势控制（食指尖上下移动）
* **Left Paddle / 左拍** — AI-controlled
  AI 自动控制
* **Goal / 目标** — Defend against the opponent’s shots and score points when they miss.
  防守对方击来的小球，并尝试让对方漏球得分
* **Score / 得分** — Unlimited
  无上限比分

---

## 📂 Project Structure / 项目结构

```
webcam-pong/
│── index.html        # Main page with game and webcam logic / 主页面，包含游戏与摄像头逻辑
│── docs/             # Docs and screenshots / 文档与截图
│── README.md         # Project description / 项目说明
```

---

## 📜 License / 许可协议

MIT License © 2025 [Your Name](https://github.com/your-username)

> This project was developed with the assistance of **GPT-5**.
> 本项目在 **GPT-5** 辅助下完成。
> Free to use, modify, and distribute, but please retain the GPT-5 acknowledgment if you fork or modify it.
> 允许自由使用、修改与分发，但若进行二次开发，请保留 GPT-5 辅助生成的声明。

---

## 💡 TODO

* [ ] Multiplayer mode / 增加多人在线对战模式
* [ ] CRT arcade filter / 添加街机风格 CRT 滤镜
* [ ] More gesture actions (e.g., serve) / 支持更多手势操作（如挥手发球）
* [ ] Mobile adaptation / 加入移动端适配

```


