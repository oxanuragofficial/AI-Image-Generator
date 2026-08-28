# 🎨 AI Image Generator

A ready-to-use AI image generation environment for Windows with a simple setup, multiple image-generation models, ControlNet support, and CivitAI model management.

> **Recommended:** NVIDIA GPU with at least 6 GB VRAM.

---

## ✨ What Is Included

This setup already contains:

* AI image generation WebUI
* SD 1.5 model
* SDXL models
* ControlNet models
* ControlNet preprocessors
* CivitAI Browser Plus
* VAE support
* Image generation tools
* txt2img
* img2img
* Extras
* PNG Info
* Checkpoint Merger
* LoRA support
* ControlNet
* OpenPose
* Canny
* Depth
* Lineart
* SoftEdge

---

# 📋 Requirements

## Windows

Windows 10/11 recommended.

## Python — REQUIRED

**Python 3.10.6 is required for this setup.**

Do **not** use Python 3.14 for this installation.

### Download Python 3.10.6

[![Download Python 3.10.6](https://img.shields.io/badge/Download-Python%203.10.6-blue?style=for-the-badge)](https://www.python.org/downloads/release/python-3106/)

During installation, enable:

```text
Add Python.exe to PATH
```

Verify:

```powershell
python --version
```

Required:

```text
Python 3.10.6
```

You can also verify the exact Python used by this setup:

```powershell
.\venv\Scripts\python.exe --version
```

Expected:

```text
Python 3.10.6
```

---

# 🚀 Quick Start

Open PowerShell inside the project folder:

```powershell
cd C:\stable-diffusion-webui
```

Then start the AI Image Generator:

```powershell
.\webui-user.bat
```

After startup, open:

```text
http://127.0.0.1:7860
```

> If your terminal shows a different local port, use the URL displayed in the terminal.

---

# 🖥️ First Launch

When the interface opens, you will see:

```text
txt2img
img2img
Extras
PNG Info
Checkpoint Merger
Train
CivitAI Browser+
Settings
Extensions
```

The main generation page is **txt2img**.

---

# 🧠 Included AI Models

The setup currently contains the following checkpoints.

## SD 1.5

### Stable Diffusion v1.5

File:

```text
models/Stable-diffusion/v1-5-pruned-emaonly.safetensors
```

Download:

[![Download SD 1.5](https://img.shields.io/badge/Download-SD%201.5-blue?style=for-the-badge)](https://huggingface.co/runwayml/stable-diffusion-v1-5)

---

## SDXL

### Juggernaut XL

File:

```text
models/Stable-diffusion/juggernautXL_ragnarok_1659952.safetensors
```

Download:

[![Download Juggernaut XL](https://img.shields.io/badge/Download-Juggernaut%20XL-purple?style=for-the-badge)](https://civitai.com/models/133005/juggernaut-xl)

---

### DreamShaper XL Lightning

File:

```text
models/Stable-diffusion/dreamshaperXL_lightningDPMSDE_282807.safetensors
```

Download:

[![Download DreamShaper XL Lightning](https://img.shields.io/badge/Download-DreamShaper%20XL-purple?style=for-the-badge)](https://civitai.com/models/112902/dreamshaper-xl-lightning)

---

## Realistic Vision

File:

```text
models/Stable-diffusion/realisticVisionV60B1_v51HyperVAE_418901.safetensors
```

Download:

[![Download Realistic Vision](https://img.shields.io/badge/Download-Realistic%20Vision-purple?style=for-the-badge)](https://civitai.com/models/4201/realistic-vision-v60-b1)

---

# 🎛️ ControlNet

ControlNet is included and already configured with the project.

Location:

```text
models/ControlNet/
```

Included ControlNet models:

| Model      | File                                 |
| ---------- | ------------------------------------ |
| Canny      | `control_v11p_sd15_canny.pth`        |
| Depth      | `control_v11f1p_sd15_depth.pth`      |
| Lineart    | `control_v11p_sd15_lineart.pth`      |
| OpenPose   | `control_v11p_sd15_openpose.pth`     |
| SoftEdge   | `control_v11p_sd15_softedge.pth`     |
| SDXL Canny | `diffusers_xl_canny_mid.safetensors` |
| SDXL Depth | `diffusers_xl_depth_mid.safetensors` |

---

# 🧩 How To Use ControlNet

1. Open **txt2img**.
2. Scroll down to **ControlNet**.
3. Enable **ControlNet Unit 0**.
4. Upload your reference image.
5. Select the appropriate **Control Type**.
6. Select the **Preprocessor**.
7. Select the ControlNet **Model**.
8. Enter your prompt.
9. Click **Generate**.

Example:

```text
Control Type:
OpenPose

Preprocessor:
OpenPose

Model:
control_v11p_sd15_openpose
```

---

# 🎯 ControlNet Model Guide

### Canny

Use for:

* Edges
* Outlines
* Preserving image structure

```text
Control Type → Canny
```

### Depth

Use for:

* 3D structure
* Depth information
* Scene composition

```text
Control Type → Depth
```

### OpenPose

Use for:

* Human poses
* Character positioning
* Body structure

```text
Control Type → OpenPose
```

### Lineart

Use for:

* Drawings
* Anime
* Sketches
* Line-based images

```text
Control Type → Lineart
```

### SoftEdge

Use for:

* Soft outlines
* Shape preservation
* Less aggressive edge control

```text
Control Type → SoftEdge
```

---

# 📁 Important Folder Structure

Do not move these folders unless you know exactly what you are changing.

```text
AI Image Generator/
│
├── models/
│   ├── Stable-diffusion/
│   │   ├── v1-5-pruned-emaonly.safetensors
│   │   ├── realisticVisionV60B1_v51HyperVAE_418901.safetensors
│   │   ├── juggernautXL_ragnarok_1659952.safetensors
│   │   └── dreamshaperXL_lightningDPMSDE_282807.safetensors
│   │
│   ├── ControlNet/
│   │   ├── control_v11p_sd15_canny.pth
│   │   ├── control_v11f1p_sd15_depth.pth
│   │   ├── control_v11p_sd15_lineart.pth
│   │   ├── control_v11p_sd15_openpose.pth
│   │   ├── control_v11p_sd15_softedge.pth
│   │   ├── diffusers_xl_canny_mid.safetensors
│   │   └── diffusers_xl_depth_mid.safetensors
│   │
│   └── VAE/
│
├── extensions/
│   ├── sd-webui-controlnet/
│   └── sd-civitai-browser-plus/
│
├── venv/
│
├── webui-user.bat
├── webui.bat
└── README.md
```

---

# ➕ Adding Another Checkpoint

Download a compatible checkpoint:

[![CivitAI](https://img.shields.io/badge/Models-CivitAI-red?style=for-the-badge)](https://civitai.com/)

or:

[![Hugging Face](https://img.shields.io/badge/Models-Hugging%20Face-yellow?style=for-the-badge)](https://huggingface.co/models)

Place the file inside:

```text
models/Stable-diffusion/
```

Supported common formats:

```text
.safetensors
.ckpt
```

Restart or refresh the WebUI checkpoint list.

---

# ➕ Adding ControlNet Models

Place ControlNet model files inside:

```text
models/ControlNet/
```

Then:

```text
Restart WebUI
        ↓
Open ControlNet
        ↓
Select Control Type
        ↓
Select Preprocessor
        ↓
Select Model
```

---

# ⚡ Faster Image Generation

For faster generation, especially on GPUs with limited VRAM:

### SDXL Lightning

Use the DreamShaper XL Lightning checkpoint.

Recommended starting settings:

```text
Sampling Steps: 4–8
Batch Size: 1
Batch Count: 1
```

For normal SDXL models, use more steps.

Do not blindly increase resolution or batch size. Both can increase VRAM usage significantly.

---

# 🎨 Basic txt2img Generation

1. Select a checkpoint.
2. Open **txt2img**.
3. Enter your prompt.
4. Set width and height.
5. Select sampling method.
6. Set sampling steps.
7. Set CFG Scale.
8. Click **Generate**.

Example:

```text
Prompt:

A cinematic portrait of a futuristic warrior,
detailed face, dramatic lighting, highly detailed,
professional photography
```

---

# 🖼️ img2img

Use **img2img** when you already have an image and want to transform or modify it.

Basic workflow:

```text
Upload image
      ↓
Write prompt
      ↓
Set Denoising Strength
      ↓
Choose resolution
      ↓
Generate
```

Higher denoising strength creates larger changes.

Lower denoising strength preserves more of the original image.

---

# 🛠️ CivitAI Browser+

The project includes:

```text
extensions/sd-civitai-browser-plus/
```

It allows you to browse and download models from CivitAI directly through the WebUI.

Open:

```text
CivitAI Browser+
```

Use it to find:

* Checkpoints
* LoRAs
* Embeddings
* Other compatible models

Always check whether a downloaded model is intended for **SD 1.5, SDXL, or another architecture** before using it.

---

# 🔄 Refreshing Models

After adding a model manually:

1. Open the checkpoint selector.
2. Click the refresh button.
3. Select the new model.

If the model does not appear:

```text
Check the file location
        ↓
Check the file extension
        ↓
Restart WebUI
```

---

# 🔍 Verify Installation

Run these commands from:

```text
C:\stable-diffusion-webui
```

### Python

```powershell
.\venv\Scripts\python.exe --version
```

Expected:

```text
Python 3.10.6
```

### PyTorch

```powershell
.\venv\Scripts\python.exe -c "import torch; print(torch.__version__); print(torch.cuda.is_available())"
```

Expected CUDA availability:

```text
True
```

### MediaPipe

```powershell
.\venv\Scripts\python.exe -c "import mediapipe as mp; print(mp.__version__); print(hasattr(mp,'solutions'))"
```

### OpenCV

```powershell
.\venv\Scripts\python.exe -c "import cv2; print(cv2.__version__)"
```

### NumPy

```powershell
.\venv\Scripts\python.exe -c "import numpy; print(numpy.__version__)"
```

---

# ❗ Important

Do **not** randomly upgrade packages inside the existing environment.

This project uses a specific working environment.

Changing packages such as:

```text
Python
PyTorch
NumPy
Gradio
OpenCV
MediaPipe
```

can break compatibility.

If everything is working, leave the environment alone.

---

# 🧯 Troubleshooting

## WebUI does not start

Run:

```powershell
.\webui-user.bat
```

Read the terminal error instead of repeatedly reinstalling packages.

---

## Checkpoint does not appear

Make sure the checkpoint is inside:

```text
models/Stable-diffusion/
```

Then restart the WebUI.

---

## ControlNet model does not appear

Make sure the model is inside:

```text
models/ControlNet/
```

Then restart the WebUI.

---

## CUDA is unavailable

Run:

```powershell
nvidia-smi
```

Then:

```powershell
.\venv\Scripts\python.exe -c "import torch; print(torch.cuda.is_available()); print(torch.cuda.get_device_name(0) if torch.cuda.is_available() else 'CUDA unavailable')"
```

---

# 📦 Project Information

WebUI version:

```text
v1.10.1
```

Python:

```text
3.10.6
```

PyTorch:

```text
2.1.2+cu121
```

Gradio:

```text
3.41.2
```

ControlNet:

```text
v1.1.455
```

---

# ⭐ Recommended Workflow

For a simple workflow:

```text
Select Checkpoint
        ↓
Write Prompt
        ↓
Set Resolution
        ↓
Set Sampling Steps
        ↓
Generate
        ↓
Use ControlNet if needed
        ↓
Upscale / Improve
        ↓
Save Image
```

For pose-controlled generation:

```text
Reference Image
        ↓
ControlNet
        ↓
OpenPose
        ↓
Prompt
        ↓
Generate
```

For structure-controlled generation:

```text
Reference Image
        ↓
ControlNet
        ↓
Canny / Depth / Lineart
        ↓
Prompt
        ↓
Generate
```

---

## 🎨 Start Creating

Run:

```powershell
.\webui-user.bat
```

Then open the local WebUI and start generating images.
