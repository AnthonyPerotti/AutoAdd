# AutoAD

Modern desktop application for automated batch video generation using FFmpeg.

AutoAD allows you to dynamically combine Hooks, Bodies and CTAs, generating large-scale video variations automatically through a modern desktop interface optimized for speed, usability and workflow automation.

---

# Features

* Modern desktop UI
* Automatic thumbnail previews
* Dynamic body management
* Batch video rendering
* Real-time render queue
* Collapsible logs and queue panels
* Persistent settings system
* Automatic output folder opening
* Responsive scrollable interface
* Instant render stop
* FFmpeg integration
* Automatic video combination system
* Professional render workflow

---

# Supported Encoders

| Encoder | Hardware |
|---|---|
| libx264 | CPU |
| h264_nvenc | NVIDIA GPU |
| h264_amf | AMD GPU |
| h264_qsv | Intel GPU |

---

# Requirements

* Python 3.14+
* FFmpeg
* CustomTkinter
* Pillow

---

# Installation

Clone repository:

```bash
git clone https://github.com/yourusername/AutoAD.git
cd AutoAD
```

Create virtual environment:

```bash
python -m venv .venv
```

Activate environment:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Running

```bash
python app.py
```

---

# Build Executable

```bash
pyinstaller ^
--onedir ^
--windowed ^
--name "AutoAD" ^
--icon="assets/icon.ico" ^
--add-data "tools;tools" ^
app.py
```

---

# Project Structure

```text
AutoAD/
│
├── app.py
├── requirements.txt
├── README.md
│
├── assets/
│   └── icon.ico
│
├── core/
│   ├── config.py
│   ├── ffmpeg.py
│   ├── render_job.py
│   ├── renderer.py
│   ├── thumbnails.py
│   ├── translations.py
│   └── state.py
│
├── ui/
│   ├── main_window.py
│   ├── hooks_panel.py
│   ├── corpos_panel.py
│   ├── cta_panel.py
│   ├── controls_panel.py
│   ├── logs_panel.py
│   ├── render_queue_panel.py
│   └── settings_window.py
│
├── tools/
│   └── ffmpeg.exe
│
├── temp/
│
└── settings.example.json
```

---

# Workflow

1. Add Hooks
2. Add Bodies
3. Add CTAs
4. Select output folder
5. Choose encoder
6. Generate videos automatically

AutoAD automatically combines all valid variations and generates the final renders in batch.

---

# AutoAD v2.0

Major rewrite including:

* Complete UI redesign
* Modular architecture
* RenderManager pipeline
* RenderJob system
* Visual render queue
* Improved FFmpeg handling
* Persistent settings
* Better responsiveness
* Improved rendering stability
* Cleaner workflow UX

---

# Notes

* FFmpeg must exist inside the `tools/` folder.
* GPU encoding depends on compatible hardware and drivers.
* `--onedir` builds are recommended for stability.
* Render queue is automatically generated during rendering sessions.

---

# License

MIT License

---

# Author

Developed by Anthony Perotti