<h1 align="center">Deep-Live-Cam (Configurable NSFW)</h1>

<p align="center">
  Real-time face swap and video deepfake with a single click and only a single image.
  <br/>
  <strong>This fork: NSFW filter is DISABLED by default and can be toggled.</strong>
</p>

---

## ⚡ Quick Start

### Default (NSFW Filter OFF)

```bash
git clone https://github.com/taiyangyu111/Deep-Live-Cam-No-NSFW.git
cd Deep-Live-Cam-No-NSFW
pip install -r requirements.txt
python run.py
```

### Enable NSFW Filter

```bash
python run.py --nsfw-filter
```

Or via environment variable:

```bash
ENABLE_NSFW_FILTER=1 python run.py
```

---

## 🎛️ Configuration

See [CONFIG.md](CONFIG.md) for detailed setup instructions.

**Key features of this fork:**
- ✅ NSFW filter **disabled by default**
- ✅ Enable via `--nsfw-filter` CLI flag
- ✅ Enable via `ENABLE_NSFW_FILTER` environment variable
- ✅ All original Deep-Live-Cam features preserved
- ✅ 100% compatible with official project

---

## 📖 Installation

### Windows

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python run.py
```

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python run.py
```

**For GPU support, see the original [Deep-Live-Cam](https://github.com/hacksider/Deep-Live-Cam) documentation.**

---

## 🚀 Usage

### GUI Mode

```bash
python run.py
```

### CLI Mode

```bash
# Basic swap (no NSFW filter)
python run.py -s source.jpg -t target.mp4 -o output.mp4

# With NSFW filter enabled
python run.py -s source.jpg -t target.mp4 --nsfw-filter
```

### Environment Variable

```bash
ENABLE_NSFW_FILTER=false python run.py    # NSFW OFF (default)
ENABLE_NSFW_FILTER=true python run.py     # NSFW ON
```

---

## 📋 What's Different?

This fork only modifies NSFW filtering behavior. Everything else is identical to the official project.

| Feature | Original | This Fork |
|---------|----------|----------|
| NSFW Filter Enabled by Default | ✓ Yes | ❌ No (OFF) |
| Can Disable NSFW Filter | ❌ No | ✓ Yes |
| CLI Flag Support | ✓ Yes | ✓ Yes |
| Environment Variable Support | ❌ No | ✓ Yes (ENABLE_NSFW_FILTER) |
| Face Swap Quality | ✓ Same | ✓ Same |
| GPU Acceleration | ✓ Yes | ✓ Yes |
| Multi-face Support | ✓ Yes | ✓ Yes |
| Live Webcam Mode | ✓ Yes | ✓ Yes |

---

## ⚖️ License & Credits

Based on [hacksider/Deep-Live-Cam](https://github.com/hacksider/Deep-Live-Cam) (AGPL-3.0)

This fork maintains the same AGPL-3.0 license and is a derivative work.

---

## 🔗 Original Project

For the full feature set and documentation, see:
- GitHub: https://github.com/hacksider/Deep-Live-Cam
- Models: https://huggingface.co/hacksider/deep-live-cam

---

## ⚠️ Disclaimer

This software is provided as-is. Users are responsible for:
- Obtaining consent when using real people's faces
- Complying with local laws and regulations
- Clearly labeling deepfakes when sharing online
- Using this tool responsibly and ethically

The authors are not responsible for misuse.
