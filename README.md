# Html To Video Pixie v1.0.0

> **Turn text prompts into videos via AI-generated HTML. No coding required.**

<p align="center">
  <img src="logo.png" width="128" alt="Html To Video Pixie Logo">
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#quick-start">Quick Start</a> •
  <a href="#how-it-works">How It Works</a> •
  <a href="#comparison">Comparison</a> •
  <a href="#download">Download</a>
</p>

---

## 📖 Overview

**Html To Video Pixie** is an AI-powered desktop application that transforms natural language descriptions into HTML/CSS animations, then renders them as high-quality MP4 videos or GIF animations.

Simply describe what you want in plain language, and the AI generates the HTML code. The built-in rendering engine converts it to video — no coding skills required.

## ✨ Features

### Core Capabilities
- **Natural Language to Video** — Describe your animation in words, get a video
- **Real-time Preview** — See the HTML animation instantly as AI generates it
- **Dual Output Formats** — Export as MP4 video or animated GIF
- **Built-in Code Editor** — Fine-tune the generated HTML directly in the app

### AI Integration
- **Multi-Model Support** — OpenAI, DeepSeek, Qwen, Zhipu AI, Xiaomi MiMo, and more
- **Custom Providers** — Add any OpenAI-compatible API service
- **Streaming Output** — Watch AI generate code in real-time

### User Experience
- **Bilingual Interface** — English and Chinese with one-click switching
- **No Installation Hassle** — Pre-packaged installer with FFmpeg included
- **Auto-save** — All creations and chat history preserved automatically
- **Import HTML** — Load existing HTML files for rendering

## 🚀 Quick Start

### Option 1: Download Installer (Recommended)
1. Download `HtmlToVideoPixieInstaller.exe`
2. Run installer (requires administrator privileges)
3. Launch from desktop shortcut or Start Menu

### Option 2: Run from Source
```bash
# Install dependencies
pip install playwright requests Pillow tkinterweb

# Install Playwright browsers
playwright install chromium

# Ensure FFmpeg is in PATH
ffmpeg -version

# Run the application
python main_tkinter.py
```

## 🎯 How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                    Html To Video Pixie                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌──────────────┐     ┌──────────────┐     ┌──────────────┐    │
│   │   User Input │ ──► │   AI Model   │ ──► │  HTML/CSS    │    │
│   │  (Natural    │     │  (GPT-4o,    │     │  Animation   │    │
│   │   Language)  │     │  DeepSeek..) │     │   Code       │    │
│   └──────────────┘     └──────────────┘     └──────┬───────┘    │
│                                                    │            │
│                                                    ▼            │
│   ┌──────────────┐     ┌──────────────┐     ┌──────────────┐    │
│   │   MP4/GIF    │ ◄── │    FFmpeg    │ ◄── │  Playwright  │    │
│   │   Output     │     │   Encoding   │     │   Browser    │    │
│   └──────────────┘     └──────────────┘     │  Rendering   │    │
│                                             └──────────────┘    │
└─────────────────────────────────────────────────────────────────┘
```

**Technical Stack:**
- **GUI**: Python tkinter (lightweight, cross-platform)
- **AI**: OpenAI-compatible API with streaming
- **Rendering**: Playwright (headless Chromium/Edge)
- **Encoding**: FFmpeg (MP4/GIF output)

## 🆚 Comparison

### vs Other HTML-to-Video Tools

| Project | Core Idea | Target Users | Tech Stack |
|---------|-----------|--------------|------------|
| **HtmlToVideoPixie** | Natural Language → HTML → Video | Non-programmers, creators | Python, Tkinter, AI API |
| Remotion | React Components → Video | Frontend developers | React, TypeScript, Node.js |
| HyperFrames | HTML Source → Video | AI Agents, developers | HTML, CSS, JavaScript |
| html-video | Data → Multi-frame HTML → Video | Automation, Coding Agents | Python, Chrome, FFmpeg |

### vs AI Video Models (Sora/Kling)

| Aspect | HtmlToVideoPixie | Sora/Kling |
|--------|------------------|------------|
| **Control** | Precise, deterministic (code-based) | Probabilistic (diffusion-based) |
| **Text Rendering** | Vector-sharp, perfect for subtitles | Often garbled/unreadable |
| **Resolution** | Unlimited (4K/8K possible) | Limited to 1080p |
| **Style** | Geometric, data-viz, presentations | Photorealistic, cinematic |
| **Editability** | Direct code editing | Re-prompt required |

### Unique Advantages
- **Exact Timing Control** — "Rotate 45° at exactly 3 seconds" is possible
- **Crystal Clear Text** — Perfect for data visualization, PPT animations, subtitles
- **Infinite Scalability** — Vector graphics scale to any resolution
- **Code-Level Precision** — Every pixel is deterministic and reproducible

## 📁 Project Structure

```
HtmlToVideoPixie/
├── main_tkinter.py          # Main application
├── installer.py             # Installer script
├── build_installer.bat      # Build script
├── logo.ico                 # Application icon
├── logo.png                 # Original logo
├── config/
│   └── providers.json       # AI provider configuration
├── core/
│   ├── ai_client.py         # AI API client
│   ├── video_generator.py   # Video rendering engine
│   └── i18n.py              # Internationalization
├── README.md                # This file
└── LICENSE                  # MIT License
```

## ⚙️ Configuration

### Adding Custom AI Providers

1. Open **Settings → Model Settings**
2. Click **Add Provider**
3. Fill in:
   - **Name**: Display name (e.g., "My DeepSeek")
   - **API URL**: Base URL (e.g., `https://api.deepseek.com/v1`)
   - **API Key**: Your API key
   - **Model ID**: Model name (e.g., `deepseek-chat`)
4. Click **Save**

Configuration is stored in `%APPDATA%\HtmlToVideoPixie\providers.json`

### Supported AI Services

- OpenAI (GPT-4o, GPT-4-turbo)
- DeepSeek (deepseek-chat, deepseek-coder)
- Qwen (qwen-turbo, qwen-plus)
- Zhipu AI (glm-4)
- Xiaomi MiMo
- Any OpenAI-compatible API

## 💡 Tips for Best Results

### Prompt Engineering

**Good Prompt:**
```
Create a colorful bar chart animation showing monthly sales data:
- 5 bars for Jan to May
- Each bar grows from bottom with a smooth ease-out animation
- Bars appear one by one with 0.3s delay
- Show value labels on top of each bar
- Use gradient colors: blue to purple
```

**Why it works:**
- Specific element count and names
- Clear animation description
- Timing parameters
- Visual style details

### Editing Workflow

1. **Generate** — Let AI create initial code
2. **Preview** — Check animation in preview pane
3. **Edit** — Adjust values in the code editor
4. **Iterate** — Regenerate if needed
5. **Export** — Save as MP4 or GIF

## 📋 System Requirements

- **OS**: Windows 10/11 (64-bit)
- **RAM**: 4GB minimum, 8GB recommended
- **Disk**: 500MB free space
- **Network**: Required for AI API calls

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| FFmpeg not found | Install FFmpeg and add to PATH |
| Browser launch failed | Run `playwright install chromium` |
| API connection error | Check API key and network |
| Video generation slow | Reduce duration/FPS in settings |

## 📄 License

MIT License - See [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

- [Playwright](https://playwright.dev/) — Browser automation
- [FFmpeg](https://ffmpeg.org/) — Video encoding
- [Pillow](https://python-pillow.org/) — Image processing
- [tkinterweb](https://tkinterweb.readthedocs.io/) — HTML preview

## 📧 Contact

- GitHub: [FatFatYoung/HtmlToVideoPixie](https://github.com/FatFatYoung/HtmlToVideoPixie)
- Issues: [Report a bug](https://github.com/FatFatYoung/HtmlToVideoPixie/issues)

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/FatFatYoung">FatFatYoung</a>
</p>
