
# 🎮 Webcam Pong

> A tribute to the classic **Pong** — powered by **GPT-5** and your webcam.  
> Real-time hand tracking with bone visualization, AI-assisted paddle control, and an 80s arcade style.  
> 致敬经典 Pong，由 GPT-5 辅助生成，通过摄像头实时手势识别控制球拍，支持骨骼可视化与 AI 辅助补位，重现 80 年代街机风格。


## 📖 Background / 开发背景

The very first video game I ever played as a child was **Pong**.  
It was simple — two paddles, one ball — yet it ignited my curiosity about games and technology.  
This project is my personal tribute to that classic, reimagined with modern technology:  
webcam-based hand tracking, AI-assisted gameplay, and retro arcade aesthetics.

我小时候玩到的第一个电子游戏就是 **Pong**。  
简单的两个球拍、一颗小球，却点燃了我对游戏和科技的好奇心。  
这个项目是我对那款经典游戏的致敬，用现代技术重现它的魅力：  

摄像头手势识别、AI 辅助对战，以及复古的街机风格。

## ✏ Prototype / 原型手稿

<img width="995" height="736" alt="prototype-sketch" src="https://github.com/user-attachments/assets/18b9d317-78c6-4329-ac08-e3f30f478e20" />


This is my original hand-drawn prototype for **Webcam Pong**.  
Before writing any code, I sketched how I imagined the game would look and function —  
from the split-screen layout (game on the left, webcam feed on the right)  
to the idea of a detection box, paddle positions, and score display.

这是我为 **Webcam Pong** 绘制的原型手稿。  
在写任何代码之前，我先画下了对游戏界面和交互方式的设想：  
左侧是游戏画面，右侧是摄像头画面；  
摄像头中有识别框，手势上下移动控制球拍；  
顶部显示实时比分，一切尽量简洁直观。

From this rough sketch, the project evolved into the fully functional version you see today,  
thanks to GPT-5’s assistance in coding, feature iteration, and debugging.

从这张简单的草图开始，在 GPT-5 的代码生成、功能迭代和调试帮助下，  
它一步步发展成了今天这个完整可玩的版本。

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

<img width="50%"  alt="webcampong" src="https://github.com/user-attachments/assets/f135f5f5-9745-4887-b500-35e6371088b0" />


## 📸 Demo 演示

| Game Screen / 游戏界面 | Camera View / 摄像头识别 |
| --- | --- |

![SCR-20250809-dnfu](https://github.com/user-attachments/assets/9d965364-0d99-4602-ba86-8f0084a5e211)


## Demo online 访问地址 




🏓 [WebCamPong](https://pong.cblink.net/ "Let'go")
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


