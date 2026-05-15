# EEG Image Reference Library & Real-time Simulation Platform

[English](#english) | [中文](#chinese)

---

<a name="english"></a>
## English

A **zero-dependency, single-file** EEG visualization toolkit for Brain-Computer Interface (BCI) research. Open `index.html` in any browser — no install, no build, no server required.

### What's inside

#### 📚 Static Reference Library
17 annotated EEG waveform cards across 3 categories:
- **Normal Rhythms** — Delta (0.5–4 Hz), Theta (4–8 Hz), Alpha (8–13 Hz), Beta (13–30 Hz), Gamma (30–100 Hz)
- **BCI Paradigms** — ERD/ERS, SSVEP, P300, ERN, MRCP, Mu Rhythm, SCP, Hybrid MI+SSVEP
- **Common Artifacts** — Eye blink, EMG, electrode pop, 50 Hz line noise

Each card includes a Canvas-rendered waveform, frequency band tag, signal description, and BCI-specific clinical context.

#### 🧠 Real-time Dynamic Simulation Platform
8-channel scrolling EEG display (10-20 system: Fp1, Fp2, F3, F4, C3, C4, O1, O2) with:
- **8 Scenario Presets** — Eyes-closed resting, Eyes-open attentive, Left/Right hand motor imagery, SSVEP 12 Hz, Sleep N2, Spike-wave discharge, EMG contamination
- **Adjustable Parameters** — Per-band gain (δ/θ/α/β/γ), global noise, amplitude scale, playback speed (0.5×/1×/2×)
- **Play/pause/reset** controls

#### 📊 Real-time Analysis Dashboard
Right-side panel with 6 analysis tools:
- **FFT Spectrum** — 0–60 Hz, 128-bin DFT with Hamming window, dB-normalized, frequency band color coding
- **Band Power Monitor** — Real-time δ/θ/α/β/γ relative power bars
- **Topographic Head Map** — 8-channel IDW spatial interpolation, selectable frequency band, blue-cyan-green-yellow-red colormap
- **Channel Selection** — Click any channel in the scrolling view to focus analysis
- **Event Injection** — One-click injection of visual stimulus, motor imagery cue, eye blink, or error response events with timeline markers
- **Data Recording** — Record up to 60 seconds of 8-channel data @ 128 Hz, auto-download as CSV

### Quick Start

```
git clone https://github.com/<your-username>/eeg-image-library.git
cd eeg-image-library
open index.html
```

Or simply download `index.html` and double-click it.

### Tech Stack

- Vanilla JavaScript (ES5-compatible, no transpiler needed)
- HTML5 Canvas (all waveform and topographic rendering)
- CSS3 (dark theme, flexbox/grid layout)
- Zero external dependencies — not even a font CDN

### Why single-file?

- **Zero friction** — Clone and open. No `npm install`, no build step.
- **Offline-first** — Works on any machine with a browser, including air-gapped lab computers.
- **Easy to audit** — One file to review, modify, or embed in other projects.
- **GitHub Pages ready** — Just enable Pages on the repo root.

### Use Cases

- BCI education and teaching
- Quick reference for EEG patterns during experiment design
- Signal simulation for algorithm prototyping
- Neurofeedback demonstration
- Public outreach and science communication

### Browser Support

| Chrome | Edge | Firefox | Safari |
|--------|------|---------|--------|
| 90+    | 90+  | 90+     | 15+    |

### Contributing

Contributions welcome! Areas where help is especially valuable:
- Additional EEG patterns and scenarios
- More 10-20 electrode positions for denser topographic maps
- Connectivity analysis (coherence, phase synchronization)
- EDF/BDF file format support
- i18n translations

### License

MIT — see [LICENSE](LICENSE)

---

<a name="chinese"></a>
## 中文

一个**零依赖、单文件**的 EEG 可视化工具集，面向脑机接口（BCI）研究。在任何浏览器中打开 `index.html` 即可使用——无需安装、无需构建、无需服务器。

### 功能概览

#### 📚 静态参考图像库
17 张带标注的 EEG 波形卡片，分 3 个类别：
- **正常节律** — Delta、Theta、Alpha、Beta、Gamma 波
- **BCI 范式** — ERD/ERS、SSVEP、P300、ERN、MRCP、μ 节律、SCP、混合 MI+SSVEP
- **常见伪迹** — 眨眼、肌电、电极弹出、50Hz 工频干扰

每张卡片包含 Canvas 渲染波形、频段标签、信号描述和 BCI 临床背景说明。

#### 🧠 动态仿真平台
8 通道实时滚动 EEG 显示（10-20 系统：Fp1、Fp2、F3、F4、C3、C4、O1、O2）：
- **8 种情境预设** — 闭眼放松、睁眼专注、左右手运动想象、SSVEP 12Hz、睡眠 N2 期、癫痫样放电、肌电干扰
- **可调参数** — 各频段增益（δ/θ/α/β/γ）、全局噪声、振幅缩放、播放速度（0.5×/1×/2×）
- **播放/暂停/重置** 控制

#### 📊 实时分析仪表盘
右侧面板包含 6 个分析工具：
- **FFT 频谱** — 0–60 Hz，128 频点 DFT、Hamming 窗、dB 标度、频段彩色标注
- **频段功率监视** — 实时 δ/θ/α/β/γ 相对功率柱状图
- **脑地形图** — 8 通道 IDW 空间插值、可选频段、蓝-青-绿-黄-红色阶
- **通道选择** — 点击滚动视图中的通道以聚焦分析
- **事件注入** — 一键注入视觉刺激、运动想象线索、眨眼、错误反应事件，带时间轴标记
- **数据录制** — 录制最多 60 秒 8 通道数据 @ 128 Hz，自动下载为 CSV

### 快速开始

```bash
git clone https://github.com/<your-username>/eeg-image-library.git
cd eeg-image-library
open index.html
```

或直接下载 `index.html` 并双击打开。

### 技术栈

- 纯 JavaScript（ES5 兼容，无需转译器）
- HTML5 Canvas（所有波形和地形图渲染）
- CSS3（暗色主题，Flexbox/Grid 布局）
- 零外部依赖

### 为什么是单文件？

- **零门槛** — 克隆即用，无需 `npm install`，无需构建步骤
- **离线可用** — 任何有浏览器的机器都能运行，包括断网的实验间电脑
- **易于审计** — 单个文件即可审查、修改或嵌入其他项目
- **GitHub Pages 即开即用** — 在仓库根目录启用 Pages 即可

### 使用场景

- BCI 教学与培训
- 实验设计时的 EEG 模式快速参考
- 算法原型开发的信号仿真
- 神经反馈演示
- 科普与公众传播

### 浏览器兼容

| Chrome | Edge | Firefox | Safari |
|--------|------|---------|--------|
| 90+    | 90+  | 90+     | 15+    |

### 参与贡献

欢迎贡献！以下方向尤其需要帮助：
- 更多 EEG 模式和情境
- 更密集的 10-20 电极位置（用于更高分辨率的地形图）
- 连接性分析（相干性、相位同步）
- EDF/BDF 文件格式支持
- 多语言翻译

### 许可证

MIT — 详见 [LICENSE](LICENSE)
