
#  AI-Powered French Flashcard App

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Flask](https://img.shields.io/badge/flask-latest-green)
![JavaScript](https://img.shields.io/badge/javascript-ES6%2B-yellow)
![FSRS](https://img.shields.io/badge/algorithm-FSRS-orange)

This is a full-stack French flashcard learning application. By combining the automated card-creation capabilities of the **Google Gemini multimodal LLM** with the cutting-edge **FSRS (Free Spaced Repetition Scheduler)** algorithm, it provides a one-stop solution for French learners—from capturing new vocabulary to achieving permanent retention.

## ✨ Core Features

### 🧠 1. AI-Powered Smart Card Generation (via Gemini 2.5 Flash)
- **Multimodal Input:** Supports uploading screenshots of French textbooks or direct text input.
- **Smart Extraction:** Automatically performs OCR and extracts key vocabulary, highlighted expressions, or contextual phrases from images.
- **Comprehensive Parsing:** Automatically generates pure French definitions, synonyms, authentic Simplified Chinese translations, and real-world bilingual context sentences (EX1, EX2).

### 📈 2. Advanced FSRS Spaced Repetition Engine
- Utilizes the native `fsrs.js` (WebAssembly) module, offering more efficient and precise memory scheduling than traditional Anki (SM-2).
- Built-in rating system: **Again**, **Hard**, **Good**, **Easy**.

### ⏱️ 3. Gamified Focus & Motivation Timer
- Built-in Pomodoro-style focus timer directly on the study interface.
- Supports dynamic target time adjustments and triggers **visual particle celebration effects** upon reaching daily goals.
- Locally records your highest records and streaks, accompanied by daily motivational quotes.

### 📝 4. Immersive "Review Mode" (Daily Recap)
- A dedicated overlay view designed for daily reviews.
- **Global Scan Mode:** Use shortcuts to instantly hide/reveal the "Definition", "Context", or "Translation" across all cards for quick self-testing.
- **Smart Auto-Centering:** The currently focused card always stays in the center of the screen when navigating with the up/down arrow keys.

### 🔄 5. Seamless Two-Way Sync & Data Persistence
- **Local-First:** Learning progress is saved in the browser's `LocalStorage` in real-time, ensuring offline availability and zero latency.
- **Backend Sync:** One-click sync to push learning data to the Python backend and persist it into an Excel database.
- **Automated Build Pipeline:** After the backend processes new vocabulary, it automatically triggers Python and Node.js scripts to rebuild the frontend JSON data source.

---

## 🛠️ Tech Stack

- **Backend:** Python, Flask, Pandas, Openpyxl, Google Generative AI (Gemini API)
- **Frontend:** Vanilla JavaScript (ES Modules), HTML5, CSS3
- **Core Algorithm:** FSRS (Free Spaced Repetition Scheduler) WASM
- **Data Storage:** Excel (`.xlsx`) as the primary database, Local Storage (`LocalStorage`), JSON (Read-only frontend data source)

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/tiannxp/An-application-for-memoring-the-French-Vocabulaires-with-FSRS
cd french-flashcard-app
```

### 2. Backend Environment Setup
Ensure you have Python 3.8+ installed.
```bash
# Install Python dependencies
pip install flask flask-cors pandas openpyxl google-generativeai
```

**Configure API Key & Paths:**
1. Get your Google Gemini API Key and set it as an environment variable:
   - Windows (CMD): `set GEMINI_API_KEY="your_api_key_here"`
   - macOS/Linux: `export GEMINI_API_KEY="your_api_key_here"`
2. Open `app.py` and modify `EXCEL_FILE_PATH` to point to your local Excel file path:
   ```python
   EXCEL_FILE_PATH = r"Your_Absolute_Path/french_app_data.xlsx"
   ```

### 3. Frontend Environment Setup
Ensure you have [Node.js](https://nodejs.org/) installed.
```bash
# Install Node dependencies (mainly to fetch fsrs.js and run build scripts)
npm install
```

### 4. Run the Application
**Start the Flask Backend Server:**
```bash
python app.py
```
**Start the Frontend:**
You can use the `Live Server` extension in VS Code, or use Python's built-in simple HTTP server in the project root directory:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000` in your browser to start learning!

---

## ⌨️ Keyboard Shortcuts Guide

To provide a seamless learning experience, this project is highly optimized for full keyboard navigation:

### Main Learning Interface
- `Space`: Flip card to show the answer / Rate as "Good"
- `1, 2, 3, 4`: Rate as Again, Hard, Good, and Easy respectively
- `Q`: Open/Close the Examples overlay
- `` ` `` (Backquote): Undo / Go back to the previous card

### Daily Review Mode
- `↑ / ↓`: Navigate up/down through the review list (auto-centers)
- `← / →`: Step-by-step reveal of definition, context, translation, and examples for a single card
- `,` (Comma): Globally toggle the display of **Definitions** for all cards
- `.` (Period): Globally toggle the display of **Contexts** for all cards
- `/` (Slash): Globally toggle the display of **Translations** for all cards
- `Esc`: Close the Review overlay or Examples overlay

---

## 📁 Core Project Structure

```text
├── app.py                      # Flask main entry (API, Gemini calls, Excel read/write)
├── script.js                   # Frontend main logic (FSRS scheduling, Timer, Shortcuts, UI)
├── index.html                  # Main UI layout
├── styles.css                  # Stylesheets (Includes particle effects & responsive layout)
├── french_app_data.xlsx        # Main Excel Database
├── data_frontend.json          # Compiled frontend question bank (Auto-generated by scripts)
├── scripts/
│   ├── build_structured_json.py # Script: Converts Excel to structured JSON
│   └── prepare_frontend_data.js # Script: Bundles frontend data
└── node_modules/               # Frontend dependencies (fsrs.js, etc.)
```

---

## 🤝 Contributing

Issues and Pull Requests are welcome to make this project even better!
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the [MIT License](LICENSE).

---
*Note: This project is not just a coding exercise, but a foreign language learning tool used in real life every day. Hope it helps you on your language journey too!*


Here is the English version of the `README.md`. It maintains the professional layout and highlights all the fantastic full-stack features of your project!

You can copy the Markdown content below and save it as your `README.md` file.

---


# 🇫🇷 AI-Powered French Flashcard App

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Flask](https://img.shields.io/badge/flask-latest-green)
![JavaScript](https://img.shields.io/badge/javascript-ES6%2B-yellow)
![FSRS](https://img.shields.io/badge/algorithm-FSRS-orange)

This is a full-stack French flashcard learning application. By combining the automated card-creation capabilities of the **Google Gemini multimodal LLM** with the cutting-edge **FSRS (Free Spaced Repetition Scheduler)** algorithm, it provides a one-stop solution for French learners—from capturing new vocabulary to achieving permanent retention.

## ✨ Core Features

### 🧠 1. AI-Powered Smart Card Generation (via Gemini 2.5 Flash)
- **Multimodal Input:** Supports uploading screenshots of French textbooks or direct text input.
- **Smart Extraction:** Automatically performs OCR and extracts key vocabulary, highlighted expressions, or contextual phrases from images.
- **Comprehensive Parsing:** Automatically generates pure French definitions, synonyms, authentic Simplified Chinese translations, and real-world bilingual context sentences (EX1, EX2).

### 📈 2. Advanced FSRS Spaced Repetition Engine
- Utilizes the native `fsrs.js` (WebAssembly) module, offering more efficient and precise memory scheduling than traditional Anki (SM-2).
- Built-in rating system: **Again**, **Hard**, **Good**, **Easy**.

### ⏱️ 3. Gamified Focus & Motivation Timer
- Built-in Pomodoro-style focus timer directly on the study interface.
- Supports dynamic target time adjustments and triggers **visual particle celebration effects** upon reaching daily goals.
- Locally records your highest records and streaks, accompanied by daily motivational quotes.

### 📝 4. Immersive "Review Mode" (Daily Recap)
- A dedicated overlay view designed for daily reviews.
- **Global Scan Mode:** Use shortcuts to instantly hide/reveal the "Definition", "Context", or "Translation" across all cards for quick self-testing.
- **Smart Auto-Centering:** The currently focused card always stays in the center of the screen when navigating with the up/down arrow keys.

### 🔄 5. Seamless Two-Way Sync & Data Persistence
- **Local-First:** Learning progress is saved in the browser's `LocalStorage` in real-time, ensuring offline availability and zero latency.
- **Backend Sync:** One-click sync to push learning data to the Python backend and persist it into an Excel database.
- **Automated Build Pipeline:** After the backend processes new vocabulary, it automatically triggers Python and Node.js scripts to rebuild the frontend JSON data source.

---

## 🛠️ Tech Stack

- **Backend:** Python, Flask, Pandas, Openpyxl, Google Generative AI (Gemini API)
- **Frontend:** Vanilla JavaScript (ES Modules), HTML5, CSS3
- **Core Algorithm:** FSRS (Free Spaced Repetition Scheduler) WASM
- **Data Storage:** Excel (`.xlsx`) as the primary database, Local Storage (`LocalStorage`), JSON (Read-only frontend data source)

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/french-flashcard-app.git
cd french-flashcard-app
```

### 2. Backend Environment Setup
Ensure you have Python 3.8+ installed.
```bash
# Install Python dependencies
pip install flask flask-cors pandas openpyxl google-generativeai
```

**Configure API Key & Paths:**
1. Get your Google Gemini API Key and set it as an environment variable:
   - Windows (CMD): `set GEMINI_API_KEY="your_api_key_here"`
   - macOS/Linux: `export GEMINI_API_KEY="your_api_key_here"`
2. Open `app.py` and modify `EXCEL_FILE_PATH` to point to your local Excel file path:
   ```python
   EXCEL_FILE_PATH = r"Your_Absolute_Path/french_app_data.xlsx"
   ```

### 3. Frontend Environment Setup
Ensure you have [Node.js](https://nodejs.org/) installed.
```bash
# Install Node dependencies (mainly to fetch fsrs.js and run build scripts)
npm install
```

### 4. Run the Application
**Start the Flask Backend Server:**
```bash
python app.py
```
**Start the Frontend:**
You can use the `Live Server` extension in VS Code, or use Python's built-in simple HTTP server in the project root directory:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000` in your browser to start learning!

---

## ⌨️ Keyboard Shortcuts Guide

To provide a seamless learning experience, this project is highly optimized for full keyboard navigation:

### Main Learning Interface
- `Space`: Flip card to show the answer / Rate as "Good"
- `1, 2, 3, 4`: Rate as Again, Hard, Good, and Easy respectively
- `Q`: Open/Close the Examples overlay
- `` ` `` (Backquote): Undo / Go back to the previous card

### Daily Review Mode
- `↑ / ↓`: Navigate up/down through the review list (auto-centers)
- `← / →`: Step-by-step reveal of definition, context, translation, and examples for a single card
- `,` (Comma): Globally toggle the display of **Definitions** for all cards
- `.` (Period): Globally toggle the display of **Contexts** for all cards
- `/` (Slash): Globally toggle the display of **Translations** for all cards
- `Esc`: Close the Review overlay or Examples overlay

---

## 📁 Core Project Structure

```text
├── app.py                      # Flask main entry (API, Gemini calls, Excel read/write)
├── script.js                   # Frontend main logic (FSRS scheduling, Timer, Shortcuts, UI)
├── index.html                  # Main UI layout
├── styles.css                  # Stylesheets (Includes particle effects & responsive layout)
├── french_app_data.xlsx        # Main Excel Database
├── data_frontend.json          # Compiled frontend question bank (Auto-generated by scripts)
├── scripts/
│   ├── build_structured_json.py # Script: Converts Excel to structured JSON
│   └── prepare_frontend_data.js # Script: Bundles frontend data
└── node_modules/               # Frontend dependencies (fsrs.js, etc.)
```

---

## 🤝 Contributing

Issues and Pull Requests are welcome to make this project even better!
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the [MIT License](LICENSE).

---
*Note: This project is not just a coding exercise, but a foreign language learning tool used in real life every day. Hope it helps you on your language journey too!*




# 🇨🇳 AI-Powered French Flashcard App (AI 驱动的法语闪卡学习系统)


![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Flask](https://img.shields.io/badge/flask-latest-green)
![JavaScript](https://img.shields.io/badge/javascript-ES6%2B-yellow)
![FSRS](https://img.shields.io/badge/algorithm-FSRS-orange)

这是一个全栈法语闪卡学习应用。它结合了 **Google Gemini 多模态大模型**的自动化制卡能力，以及先进的 **FSRS (Free Spaced Repetition Scheduler)** 间隔重复算法，旨在为法语学习者提供从“生词捕获”到“永久记忆”的一站式解决方案。

## ✨ 核心特性

### 🧠 1. AI 智能自动化制卡 (基于 Gemini 2.5 Flash)
- **多模态输入**：支持上传法语教材截图或直接输入文本。
- **智能提取**：自动 OCR 并提取图片中的重点词汇、高亮表达或语境短语。
- **自动全维度解析**：自动生成纯法语释义、近义词、纯正简体中文翻译，并配上包含中法对照的真实语境例句（EX1, EX2）。

### 📈 2. 先进的 FSRS 记忆算法引擎
- 采用原生的 `fsrs.js` (WebAssembly) 模块，提供比传统 Anki (SM-2) 更高效、更精准的记忆调度。
- 评分系统：**重来 (Again)**、**困难 (Hard)**、**良好 (Good)**、**简单 (Easy)**。

### ⏱️ 3. 游戏化专注激励计时器
- 内置番茄钟风格的专注计时器。
- 支持动态调节目标时间，达成目标后触发**视觉粒子庆祝特效**。
- 本地记录最高纪录和连胜状态，提供每日激励名言。

### 📝 4. 沉浸式“今日回顾”模式 (Review Mode)
- 专为每日复习设计的浮层视图。
- **全局扫描模式**：通过快捷键一键隐藏/显示所有卡片的“定义”、“语境”或“翻译”，方便自测。
- **智能居中滚动**：键盘上下导航时，当前聚焦的卡片始终保持在屏幕中央。

### 🔄 5. 无缝的双向数据同步与持久化
- **本地优先**：学习进度实时保存在浏览器的 `LocalStorage` 中，确保离线可用。
- **后端同步**：一键将学习数据同步至 Python 后端，并持久化写入 Excel 数据库。
- **自动化构建**：后端处理完新词后，自动触发 Python 和 Node.js 脚本重建前端 JSON 数据源。

---

## 🛠️ 技术栈

- **后端 (Backend)**: Python, Flask, Pandas, Openpyxl, Google Generative AI (Gemini API)
- **前端 (Frontend)**: 原生 JavaScript (ES Modules), HTML5, CSS3
- **核心算法**: FSRS (Free Spaced Repetition Scheduler) WASM
- **数据存储**: Excel (`.xlsx`) 作为主数据库, 本地存储 (`LocalStorage`), JSON (前端数据源)

---

## 🚀 快速开始

### 1. 克隆项目
```bash
git clone git clone https://github.com/tiannxp/An-application-for-memoring-the-French-Vocabulaires-with-FSRS
cd french-flashcard-app
```

### 2. 后端环境配置
确保您已安装 Python 3.8+。
```bash
# 安装 Python 依赖
pip install flask flask-cors pandas openpyxl google-generativeai
```

**配置 API Key 与路径：**
1. 获取您的 Google Gemini API Key，并设置为环境变量：
   - Windows (CMD): `set GEMINI_API_KEY="your_api_key_here"`
   - macOS/Linux: `export GEMINI_API_KEY="your_api_key_here"`
2. 打开 `app.py`，修改 `EXCEL_FILE_PATH` 为您本地的 Excel 文件路径：
   ```python
   EXCEL_FILE_PATH = r"您的绝对路径/french_app_data.xlsx"
   ```

### 3. 前端环境配置
确保您已安装 [Node.js](https://nodejs.org/)。
```bash
# 安装前端依赖 (主要为了获取 fsrs.js 和执行构建脚本)
npm install
```

### 4. 运行应用
**启动 Flask 后端服务器：**
```bash
python app.py
```
**启动前端：**
可以使用 VS Code 的 `Live Server` 插件，或使用 Python 自带的简易服务器在项目根目录下运行：
```bash
python -m http.server 8000
```
然后访问 `http://localhost:8000` 即可开始学习！

---

## ⌨️ 快捷键指南

为了提供流畅无缝的学习体验，本项目深度优化了全键盘操作：

### 主学习界面
- `Space (空格键)`: 翻转卡片显示答案 / 评级为“良好(Good)”
- `1, 2, 3, 4`: 分别对应评分 重来、困难、良好、简单
- `Q`: 呼出/关闭例句(Examples)浮层
- `\`` (反引号): 撤销/返回上一张卡片

### 今日回顾模式 (Review Mode)
- `↑ / ↓`: 上下切换当前聚焦的复习卡片（自动居中）
- `← / →`: 逐步揭示单张卡片的定义、语境、翻译和例句
- `, (逗号)`: 全局切换所有卡片的**定义**显示状态
- `. (句号)`: 全局切换所有卡片的**语境**显示状态
- `/ (斜杠)`: 全局切换所有卡片的**翻译**显示状态
- `Esc`: 关闭回顾面板或例句面板

---

## 📁 核心项目结构

```text
├── app.py                      # Flask 主程序 (处理API、调用Gemini、Excel读写)
├── script.js                   # 前端主逻辑 (FSRS调度、专注计时器、快捷键、UI交互)
├── index.html                  # 前端主界面
├── styles.css                  # 样式文件 (包含粒子动画和响应式布局)
├── french_app_data.xlsx        # Excel 主数据库 (自动生成与维护)
├── data_frontend.json          # 编译后的前端只读题库 (由脚本自动生成)
├── scripts/
│   ├── build_structured_json.py # 数据转换脚本 (Excel -> 结构化 JSON)
│   └── prepare_frontend_data.js # 前端数据打包脚本
└── node_modules/               # 存放 fsrs.js 等前端依赖
```

---

## 🤝 参与贡献

欢迎提交 Issue 和 Pull Request 来完善这个项目！
1. Fork 本仓库
2. 创建您的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交您的修改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送至分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

## 📄 许可证

本项目采用 [MIT License](LICENSE) 许可证。

---
*注：本项目不仅是一个代码练习，更是每天真实使用的外语学习工具。愿它也能帮到正在学习语言的你！*
