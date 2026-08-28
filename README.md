# 🎨 AI Image Generator

A ready-to-use **AI Image Generator for Windows** with multiple image-generation models, ControlNet, CivitAI Browser+, and support for both SD 1.5 and SDXL workflows.

---

## ✨ Features

* 🖼️ Text-to-Image generation
* 🔄 Image-to-Image generation
* 🎨 Multiple AI checkpoints
* 🎛️ ControlNet
* 🧍 OpenPose
* ✏️ Canny
* 🖌️ Lineart
* 🌊 SoftEdge
* 🏔️ Depth
* ⚡ SDXL Lightning generation
* 📦 CivitAI Browser+
* 🔍 PNG Info
* 🛠️ Extras
* 🔀 Checkpoint Merger
* 🎯 LoRA support

---

# 💻 Requirements

### Operating System

* Windows 10
* Windows 11

### GPU

An NVIDIA GPU is strongly recommended.

For SDXL, **8 GB+ VRAM is recommended**.

The setup can work with lower VRAM using appropriate settings, but generation will be slower and some models may require VRAM optimization.

---

# 🐍 Python Requirement

## ⚠️ Python 3.10.6 REQUIRED

This setup uses:

```text
Python 3.10.6
```

**Do not use Python 3.14 for this setup.**

Download Python 3.10.6:

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

---

# 📥 Download the Project

Clone the repository:

```powershell
git clone https://github.com/oxanuragofficial/AI-Image-Generator.git
```

Enter the folder:

```powershell
cd AI-Image-Generator
```

---

# 🚀 Start the AI Image Generator

Run:

```powershell
.\webui-user.bat
```

After startup, open the local address shown in the terminal.

Usually:

```text
http://127.0.0.1:7860
```

---

# 🧠 AI Models

The project supports both **SD 1.5** and **SDXL** models.

## SD 1.5

### Stable Diffusion v1.5

Download:

[![Download SD 1.5](https://img.shields.io/badge/Download-Stable%20Diffusion%201.5-blue?style=for-the-badge)](https://huggingface.co/runwayml/stable-diffusion-v1-5)

Place the checkpoint in:

```text
models/Stable-diffusion/
```

---

## SDXL

### Juggernaut XL

Download:

[![Download Juggernaut XL](https://img.shields.io/badge/Download-Juggernaut%20XL-purple?style=for-the-badge)](https://civitai.com/models/133005/juggernaut-xl)

Place the file in:

```text
models/Stable-diffusion/
```

---

### DreamShaper XL Lightning

Download:

[![Download DreamShaper XL Lightning](https://img.shields.io/badge/Download-DreamShaper%20XL%20Lightning-purple?style=for-the-badge)](https://civitai.com/models/112902/dreamshaper-xl-lightning)

Place the file in:

```text
models/Stable-diffusion/
```

This model is useful when you want **faster SDXL generation**.

---

### Realistic Vision

Download:

[![Download Realistic Vision](https://img.shields.io/badge/Download-Realistic%20Vision-purple?style=for-the-badge)](https://civitai.com/models/4201/realistic-vision-v60-b1)

Place the file in:

```text
models/Stable-diffusion/
```

---

# 📂 Model Folder

All checkpoints should be placed here:

```text
AI-Image-Generator/
└── models/
    └── Stable-diffusion/
```

Example:

```text
models/
└── Stable-diffusion/
    ├── v1-5-pruned-emaonly.safetensors
    ├── realisticVisionV60B1_v51HyperVAE_418901.safetensors
    ├── juggernautXL_ragnarok_1659952.safetensors
    └── dreamshaperXL_lightningDPMSDE_282807.safetensors
```

After adding a model, restart the WebUI or refresh the checkpoint list.

---

# 🎛️ ControlNet

ControlNet is included in the project.

Folder:

```text
models/ControlNet/
```

## Included ControlNet Models

| ControlNet | Model                                |
| ---------- | ------------------------------------ |
| Canny      | `control_v11p_sd15_canny.pth`        |
| Depth      | `control_v11f1p_sd15_depth.pth`      |
| Lineart    | `control_v11p_sd15_lineart.pth`      |
| OpenPose   | `control_v11p_sd15_openpose.pth`     |
| SoftEdge   | `control_v11p_sd15_softedge.pth`     |
| SDXL Canny | `diffusers_xl_canny_mid.safetensors` |
| SDXL Depth | `diffusers_xl_depth_mid.safetensors` |

---

# 📥 ControlNet Downloads

If you need to reinstall the ControlNet models:

### Canny

[![Download Canny](https://img.shields.io/badge/Download-ControlNet%20Canny-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/ControlNet-v1-1)

### Depth

[![Download Depth](https://img.shields.io/badge/Download-ControlNet%20Depth-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/ControlNet-v1-1)

### OpenPose

[![Download OpenPose](https://img.shields.io/badge/Download-ControlNet%20OpenPose-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/ControlNet-v1-1)

### Lineart

[![Download Lineart](https://img.shields.io/badge/Download-ControlNet%20Lineart-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/ControlNet-v1-1)

### SoftEdge

[![Download SoftEdge](https://img.shields.io/badge/Download-ControlNet%20SoftEdge-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/ControlNet-v1-1)

---

# 🧩 ControlNet Setup

Open:

```text
txt2img
```

Scroll to:

```text
ControlNet
```

Then:

1. Enable **ControlNet Unit 0**
2. Upload your reference image
3. Select the appropriate Control Type
4. Select the Preprocessor
5. Select the ControlNet Model
6. Set Control Weight
7. Enter your prompt
8. Click **Generate**

---

# 🎯 Which ControlNet Should I Use?

## 🧍 OpenPose

Best for:

* Human poses
* Character positioning
* Body posture

Use:

```text
Control Type → OpenPose
```

---

## ✏️ Canny

Best for:

* Edges
* Outlines
* Structure preservation

Use:

```text
Control Type → Canny
```

---

## 🏔️ Depth

Best for:

* 3D structure
* Scene depth
* Spatial composition

Use:

```text
Control Type → Depth
```

---

## 🖌️ Lineart

Best for:

* Sketches
* Anime
* Drawings
* Line-based references

Use:

```text
Control Type → Lineart
```

---

## 🌊 SoftEdge

Best for:

* Soft outlines
* General shape preservation
* Less aggressive edge control

Use:

```text
Control Type → SoftEdge
```

---

# ⚡ Fast Generation

For faster generation, use:

### DreamShaper XL Lightning

Start with:

```text
Sampling Steps: 4–8
Batch Size: 1
Batch Count: 1
```

Avoid unnecessarily large resolutions.

Higher resolution and larger batch sizes consume significantly more VRAM.

---

# 🖼️ Basic Image Generation

Open:

```text
txt2img
```

Then:

```text
1. Select checkpoint
2. Enter prompt
3. Set Width / Height
4. Select Sampling Method
5. Set Sampling Steps
6. Set CFG Scale
7. Click Generate
```

Example prompt:

```text
A cinematic portrait of a futuristic warrior,
dramatic lighting, detailed face,
professional photography, highly detailed
```

---

# 🔄 Image-to-Image

Use:

```text
img2img
```

Workflow:

```text
Upload Image
      ↓
Enter Prompt
      ↓
Set Denoising Strength
      ↓
Generate
```

Lower denoising strength:

```text
More similarity to original image
```

Higher denoising strength:

```text
More transformation
```

---

# 📦 CivitAI Browser+

The project includes:

```text
extensions/sd-civitai-browser-plus/
```

CivitAI:

[![Open CivitAI](https://img.shields.io/badge/Open-CivitAI-red?style=for-the-badge)](https://civitai.com/)

Use CivitAI Browser+ to discover and download additional:

* Checkpoints
* LoRAs
* Embeddings
* Other compatible models

Always check the model architecture before downloading.

For example:

```text
SD 1.5 model → SD 1.5 workflow
SDXL model   → SDXL workflow
```

---

# 🧰 ControlNet Extension

The project includes:

```text
extensions/sd-webui-controlnet/
```

The extension provides the ControlNet interface and preprocessors.

If ControlNet does not appear:

```text
Restart WebUI
```

Then check:

```text
Extensions
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

### PyTorch + CUDA

```powershell
.\venv\Scripts\python.exe -c "import torch; print('Torch:', torch.__version__); print('CUDA:', torch.cuda.is_available()); print('GPU:', torch.cuda.get_device_name(0) if torch.cuda.is_available() else 'Not detected')"
```

CUDA should report:

```text
CUDA: True
```

### MediaPipe

```powershell
.\venv\Scripts\python.exe -c "import mediapipe as mp; print('MediaPipe:', mp.__version__); print('Solutions:', hasattr(mp,'solutions'))"
```

### OpenCV

```powershell
.\venv\Scripts\python.exe -c "import cv2; print('OpenCV:', cv2.__version__)"
```

### NumPy

```powershell
.\venv\Scripts\python.exe -c "import numpy; print('NumPy:', numpy.__version__)"
```

---

# ⚠️ Do Not Randomly Upgrade Packages

This setup depends on a compatible Python environment.

Avoid randomly upgrading:

```text
Python
PyTorch
NumPy
Gradio
OpenCV
MediaPipe
```

If the current installation works, **leave the environment unchanged**.

---

# 🗂️ Project Structure

```text
AI-Image-Generator/
│
├── models/
│   ├── Stable-diffusion/
│   ├── ControlNet/
│   └── VAE/
│
├── extensions/
│   ├── sd-webui-controlnet/
│   └── sd-civitai-browser-plus/
│
├── modules/
├── scripts/
├── configs/
│
├── webui-user.bat
├── webui.bat
├── config.json
├── ui-config.json
└── README.md
```

> The GitHub repository intentionally does **not** contain the large model files, Python virtual environment, or downloaded dependency repositories. These are excluded from Git to keep the repository manageable.

---

# 🧯 Troubleshooting

## Python version is wrong

Check:

```powershell
.\venv\Scripts\python.exe --version
```

Required:

```text
Python 3.10.6
```

---

## Model is not showing

Check that the model is inside:

```text
models/Stable-diffusion/
```

Then restart WebUI.

---

## ControlNet model is not showing

Check:

```text
models/ControlNet/
```

Then restart WebUI.

---

## CUDA is not detected

Run:

```powershell
nvidia-smi
```

Then:

```powershell
.\venv\Scripts\python.exe -c "import torch; print(torch.cuda.is_available())"
```

If it returns:

```text
False
```

your GPU/PyTorch environment needs troubleshooting.

---

# 📌 Current Environment

```text
AI Image Generator
WebUI: v1.10.1
Python: 3.10.6
PyTorch: 2.1.2+cu121
Gradio: 3.41.2
ControlNet: v1.1.455
```

---

# 🎨 Start Generating

Run:

```powershell
.\webui-user.bat
```

Open the local WebUI shown in the terminal.

Select a model, write your prompt, configure your settings, and click:

```text
Generate
```

**Enjoy creating. 🎨**
