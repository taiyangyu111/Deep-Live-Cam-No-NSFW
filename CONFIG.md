# Deep-Live-Cam (Configurable NSFW)

## NSFW Filter Configuration

This is a modified version of Deep-Live-Cam with **configurable NSFW filtering**.

**Default behavior: NSFW filter is DISABLED**

You have 3 ways to control NSFW filtering:

### 1. Environment Variable (Recommended)

Create a `.env` file in the project root:

```bash
cp .env.example .env
```

Edit `.env` and set:

```bash
ENABLE_NSFW_FILTER=false    # Disabled (default)
# or
ENABLE_NSFW_FILTER=true     # Enabled
```

Then run:

```bash
python run.py
```

### 2. Command-Line Flag

Enable NSFW filtering via CLI:

```bash
python run.py --nsfw-filter
```

Without the flag, filtering is disabled.

### 3. Both

Environment variable sets the default. CLI flag overrides it:

```bash
ENABLE_NSFW_FILTER=true python run.py         # Filter enabled
ENABLE_NSFW_FILTER=true python run.py         # Filter still enabled
```

---

## Installation

Same as the official Deep-Live-Cam:

```bash
# Clone
git clone https://github.com/taiyangyu111/Deep-Live-Cam-No-NSFW.git
cd Deep-Live-Cam-No-NSFW

# Virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt

# Download models
# Place gfpgan-1024.onnx and inswapper_128_fp16.onnx in ./models/ folder

# Run
python run.py
```

## Command Line Usage

All original Deep-Live-Cam CLI flags still work:

```bash
python run.py -s face.jpg -t video.mp4 -o output.mp4
python run.py -s face.jpg -t video.mp4 --nsfw-filter    # With NSFW enabled
```

## Supported Filters

- `ENABLE_NSFW_FILTER=1` ✓
- `ENABLE_NSFW_FILTER=true` ✓
- `ENABLE_NSFW_FILTER=yes` ✓
- `ENABLE_NSFW_FILTER=on` ✓
- `ENABLE_NSFW_FILTER=false` (default) ✓
- `ENABLE_NSFW_FILTER=0` (same as false) ✓

## What's Different?

| Feature | Original | This Fork |
|---------|----------|----------|
| NSFW Filter Default | On (hardcoded) | **Off (configurable)** |
| Enable via CLI | `--nsfw-filter` only turns it on | `--nsfw-filter` enables it |
| Enable via Env | ❌ Not available | ✓ `ENABLE_NSFW_FILTER=1` |
| All Other Features | ✓ Yes | ✓ Yes (100% compatible) |

---

## Credits

Based on the official [hacksider/Deep-Live-Cam](https://github.com/hacksider/Deep-Live-Cam)

This fork only adds configurable filtering — all credit for the core technology goes to the original authors.
