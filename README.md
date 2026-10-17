# 🌆 Sonic City

[![Support on Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nytmaer)

A retro-futuristic audio visualizer that transforms music into a living, breathing cyberpunk cityscape. Built with **Three.js** and the **Web Audio API**.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Three.js](https://img.shields.io/badge/Three.js-r128-black.svg)
![Tailwind](https://img.shields.io/badge/Tailwind-CSS-38B2AC.svg)

## 🎵 Concept

Sonic City visualizes audio as a rotating metropolitan landscape:
- **The Sun** (tennis ball) sits at the center, pulsing to the beat
- **The Record** (vinyl) serves as the base platform
- **The City** (abstract buildings) rise and fall with frequency data
  - Inner rings = Sub-bass/Bass
  - Outer rings = Mids/Highs

## 🚀 Live Demo

[View Live Demo](https://nytmaer.github.io/sonic-city) *(GitHub Pages)*

## 🎮 Controls

| Key | Action |
|-----|--------|
| `H` | Toggle HUD |
| `Scroll` | Zoom in/out |
| `Click` | Initialize audio context |

### UI Features
- **Microphone Input**: Real-time visualization from device mic
- **File Upload**: Drag & drop audio files (MP3, WAV)
- **Sensitivity**: Adjust building reaction intensity (0.5x - 3x)
- **Smoothing**: Control audio reactivity lag
- **Visual Toggles**: Grid floor, auto-rotation, particles

## 🛠️ Technical Details

### Audio Processing
- **FFT Size**: 256 bins for frequency analysis
- **Beat Detection**: Real-time BPM estimation using low-frequency energy analysis
- **Frequency Mapping**: 4-zone spectral analysis (Sub/Bass/Mid/High)

### Visual Engine
- **Camera**: Perspective 60° FOV, positioned at (0, 60, 140)
- **Lighting**: Ambient + 3-point rim lighting (Cyan/Magenta/White)
- **Materials**: PBR with emissive glow for neon aesthetic
- **Post-processing**: Fog for depth, tone mapping for HDR

### Performance
- 80 buildings total (instanced groups)
- 2,000 particle stars
- 60 FPS target on modern devices

## 📦 Installation

No build process required! This is a vanilla JavaScript application.

```bash
git clone https://github.com/nytmaer/sonic-city-visualizer.git
cd sonic-city-visualizer
# Open index.html in a browser or serve with:
python -m http.server 8000

## Support

If you find this project useful, you can support its development on Ko-fi: **[ko-fi.com/nytmaer](https://ko-fi.com/nytmaer)**
