# Stable Diffusion web UI
A web interface for Stable Diffusion, implemented using Gradio library.

![](screenshot.png)

# Stable Diffusion WebUI — Complete Windows Setup

> A ready-to-use **AUTOMATIC1111 Stable Diffusion WebUI v1.10.1** setup for Windows with **ControlNet**, **CivitAI Browser+**, SD 1.5 models and SDXL models.

[![Python](https://img.shields.io/badge/Python-3.10.6-blue?style=for-the-badge\&logo=python)](https://www.python.org/downloads/release/python-3106/)
[![WebUI](https://img.shields.io/badge/AUTOMATIC1111-v1.10.1-black?style=for-the-badge)](https://github.com/AUTOMATIC1111/stable-diffusion-webui)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.1.2%20%2B%20CUDA%2012.1-ee4c2c?style=for-the-badge\&logo=pytorch)](https://pytorch.org/)
[![ControlNet](https://img.shields.io/badge/ControlNet-v1.1.455-blue?style=for-the-badge)](https://github.com/Mikubill/sd-webui-controlnet)

---

# 📌 What This Repository Contains

This repository contains the WebUI setup and extensions.

### Included

* AUTOMATIC1111 WebUI `v1.10.1`
* ControlNet `v1.1.455`
* CivitAI Browser+
* WebUI configuration
* ControlNet extension files
* CivitAI Browser+ extension files
* Required project source files

### NOT included

Large files are intentionally excluded from GitHub:

* `venv/`
* `models/`
* `repositories/`
* `config_states/`

You download the models separately and place them into the correct folders.

---

# ⚠️ IMPORTANT — Python Version

## Python 3.10.6 is REQUIRED

This setup was built and tested with:

```text
Python 3.10.6
```

**Do not use Python 3.11, 3.12, 3.13 or 3.14 for this setup.**

### Download Python 3.10.6

[![DOWNLOAD PYTHON 3.10.6](https://img.shields.io/badge/⬇%20DOWNLOAD-PYTHON%203.10.6-blue?style=for-the-badge)](https://www.python.org/downloads/release/python-3106/)

During installation:

```text
☑ Add Python 3.10 to PATH
```

### Verify

Open PowerShell:

```powershell
python --version
```

It must return:

```text
Python 3.10.6
```

Also check:

```powershell
py -3.10 --version
```

Expected:

```text
Python 3.10.6
```

If you get another version, **do not continue until Python 3.10.6 is available.**

---

# 1️⃣ Install Git

Git is required to download this repository.

[![DOWNLOAD GIT](https://img.shields.io/badge/⬇%20DOWNLOAD-GIT-orange?style=for-the-badge\&logo=git)](https://git-scm.com/download/win)

Verify:

```powershell
git --version
```

---

# 2️⃣ Clone This Repository

Open PowerShell:

```powershell
cd C:\
```

Clone:

```powershell
git clone https://github.com/oxanuragofficial/stable-diffusion-webui-setup.git
```

Enter the directory:

```powershell
cd C:\stable-diffusion-webui-setup
```

Your installation directory can be different.

Example:

```text
D:\AI\stable-diffusion-webui-setup
```

---

# 3️⃣ NVIDIA GPU Check

For NVIDIA GPUs, verify that Windows can see your GPU:

```powershell
nvidia-smi
```

You should see your NVIDIA GPU, driver and VRAM information.

This setup was tested with:

```text
PyTorch: 2.1.2+cu121
CUDA build: 12.1
```

---

# 4️⃣ Start WebUI

From the repository directory:

```powershell
.\webui-user.bat
```

The first launch may take some time because WebUI creates the Python environment and installs dependencies.

When startup completes, you should see something similar to:

```text
Running on local URL: http://127.0.0.1:7860
```

Open that address in your browser.

---

# 5️⃣ Model Folder Structure

You will use these folders:

```text
stable-diffusion-webui-setup/
│
├── models/
│   │
│   ├── Stable-diffusion/
│   │
│   ├── ControlNet/
│   │
│   └── VAE/
│
├── extensions/
│   │
│   ├── sd-webui-controlnet/
│   │
│   └── sd-civitai-browser-plus/
│
└── webui-user.bat
```

If a folder does not exist, create it manually.

---

# 6️⃣ Stable Diffusion Checkpoints

## Where do checkpoints go?

All `.safetensors` checkpoints go here:

```text
models\Stable-diffusion\
```

Example:

```text
models/
└── Stable-diffusion/
    ├── v1-5-pruned-emaonly.safetensors
    ├── realisticVisionV60B1_v51HyperVAE_418901.safetensors
    ├── dreamshaperXL_lightningDPMSDE_282807.safetensors
    └── juggernautXL_ragnarok_1659952.safetensors
```

---

# 7️⃣ SD 1.5 — Base Model

## `v1-5-pruned-emaonly.safetensors`

This is the SD 1.5 base checkpoint.

### Download

[![DOWNLOAD SD 1.5](https://img.shields.io/badge/⬇%20DOWNLOAD-SD%201.5-blue?style=for-the-badge)](https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5/blob/main/v1-5-pruned-emaonly.safetensors)

The official model page lists the `v1-5-pruned-emaonly.safetensors` file.

### Put it here

```text
models\Stable-diffusion\v1-5-pruned-emaonly.safetensors
```

---

# 8️⃣ Realistic Vision V6

## `realisticVisionV60B1_v51HyperVAE_418901.safetensors`

This is an SD 1.5-family realistic checkpoint.

### Download

[![DOWNLOAD REALISTIC VISION](https://img.shields.io/badge/⬇%20DOWNLOAD-REALISTIC%20VISION-purple?style=for-the-badge)](https://civitai.com/)

Search for:

```text
Realistic Vision V6.0 B1
```

### Put it here

```text
models\Stable-diffusion\realisticVisionV60B1_v51HyperVAE_418901.safetensors
```

> **Note:** CivitAI model pages and file IDs can change. Use the model's official CivitAI page rather than downloading an unknown mirror.

---

# 9️⃣ DreamShaper XL Lightning

## `dreamshaperXL_lightningDPMSDE_282807.safetensors`

This is an **SDXL** checkpoint.

### Download

[![DOWNLOAD DREAMSHAPER XL](https://img.shields.io/badge/⬇%20DOWNLOAD-DREAMSHAPER%20XL-purple?style=for-the-badge)](https://civitai.com/)

Search:

```text
DreamShaper XL Lightning
```

### Put it here

```text
models\Stable-diffusion\dreamshaperXL_lightningDPMSDE_282807.safetensors
```

---

# 🔟 Juggernaut XL Ragnarok

## `juggernautXL_ragnarok_1659952.safetensors`

This is an **SDXL** checkpoint.

### Download

[![DOWNLOAD JUGGERNAUT XL](https://img.shields.io/badge/⬇%20DOWNLOAD-JUGGERNAUT%20XL-purple?style=for-the-badge)](https://civitai.com/)

Search:

```text
Juggernaut XL Ragnarok
```

### Put it here

```text
models\Stable-diffusion\juggernautXL_ragnarok_1659952.safetensors
```

---

# 1️⃣1️⃣ ControlNet

ControlNet is already included in this repository.

Location:

```text
extensions\sd-webui-controlnet\
```

Your setup uses:

```text
ControlNet v1.1.455
```

The official ControlNet v1.1 model family includes dedicated models for Canny, Depth, OpenPose, SoftEdge, Lineart and other conditioning types.

---

# 1️⃣2️⃣ ControlNet Model Folder

Create:

```text
models\ControlNet\
```

Your SD 1.5 ControlNet models go there.

Final structure:

```text
models/
└── ControlNet/
    │
    ├── control_v11p_sd15_canny.pth
    ├── control_v11f1p_sd15_depth.pth
    ├── control_v11p_sd15_lineart.pth
    ├── control_v11p_sd15_openpose.pth
    └── control_v11p_sd15_softedge.pth
```

---

# 1️⃣3️⃣ ControlNet — Canny

### File

```text
control_v11p_sd15_canny.pth
```

### Download

[![DOWNLOAD CANNY](https://img.shields.io/badge/⬇%20DOWNLOAD-CANNY-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/control_v11p_sd15_canny)

### Put here

```text
models\ControlNet\control_v11p_sd15_canny.pth
```

### Use for

* Strong edges
* Object outlines
* Composition
* Shape preservation

---

# 1️⃣4️⃣ ControlNet — Depth

### File

```text
control_v11f1p_sd15_depth.pth
```

### Download

[![DOWNLOAD DEPTH](https://img.shields.io/badge/⬇%20DOWNLOAD-DEPTH-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/control_v11f1p_sd15_depth)

### Put here

```text
models\ControlNet\control_v11f1p_sd15_depth.pth
```

### Use for

* 3D structure
* Foreground/background separation
* Maintaining spatial composition
* Controlling scene depth

The official model description identifies the depth model as the SD1.5 ControlNet trained using depth estimation.

---

# 1️⃣5️⃣ ControlNet — OpenPose

### File

```text
control_v11p_sd15_openpose.pth
```

### Download

[![DOWNLOAD OPENPOSE](https://img.shields.io/badge/⬇%20DOWNLOAD-OPENPOSE-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/control_v11p_sd15_openpose)

### Put here

```text
models\ControlNet\control_v11p_sd15_openpose.pth
```

### Use for

* Human pose
* Body position
* Character positioning
* Dance/action poses

The official model is specifically trained for OpenPose conditioning.

---

# 1️⃣6️⃣ ControlNet — Lineart

### File

```text
control_v11p_sd15_lineart.pth
```

### Download

[![DOWNLOAD LINEART](https://img.shields.io/badge/⬇%20DOWNLOAD-LINEART-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/control_v11p_sd15_lineart)

### Put here

```text
models\ControlNet\control_v11p_sd15_lineart.pth
```

### Use for

* Drawings
* Sketches
* Illustration structure
* Clean outlines

---

# 1️⃣7️⃣ ControlNet — SoftEdge

### File

```text
control_v11p_sd15_softedge.pth
```

### Download

[![DOWNLOAD SOFTEDGE](https://img.shields.io/badge/⬇%20DOWNLOAD-SOFTEDGE-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/control_v11p_sd15_softedge)

### Put here

```text
models\ControlNet\control_v11p_sd15_softedge.pth
```

### Use for

* Soft outlines
* Structure preservation
* Artistic edges
* Less rigid composition control

---

# 1️⃣8️⃣ SDXL ControlNet Models

Your setup also contains:

```text
diffusers_xl_canny_mid.safetensors
diffusers_xl_depth_mid.safetensors
```

These are **SDXL ControlNet models**, not SD1.5 ControlNet models.

The official SDXL ControlNet collection includes separate Canny and Depth models in small, mid and full variants.

### Canny SDXL

[![DOWNLOAD SDXL CANNY](https://img.shields.io/badge/⬇%20DOWNLOAD-SDXL%20CANNY-blue?style=for-the-badge)](https://huggingface.co/diffusers/controlnet-canny-sdxl-1.0-mid)

### Depth SDXL

[![DOWNLOAD SDXL DEPTH](https://img.shields.io/badge/⬇%20DOWNLOAD-SDXL%20DEPTH-blue?style=for-the-badge)](https://huggingface.co/diffusers/controlnet-depth-sdxl-1.0-mid)

Put them here:

```text
models\ControlNet\
```

Result:

```text
models/
└── ControlNet/
    ├── control_v11p_sd15_canny.pth
    ├── control_v11f1p_sd15_depth.pth
    ├── control_v11p_sd15_lineart.pth
    ├── control_v11p_sd15_openpose.pth
    ├── control_v11p_sd15_softedge.pth
    ├── diffusers_xl_canny_mid.safetensors
    └── diffusers_xl_depth_mid.safetensors
```

---

# 1️⃣9️⃣ ControlNet Configuration

Start WebUI:

```powershell
.\webui-user.bat
```

Open:

```text
txt2img
```

Scroll down until you see:

```text
ControlNet
```

You should see:

```text
ControlNet Unit 0
ControlNet Unit 1
ControlNet Unit 2
```

---

## Step 1 — Enable ControlNet

Open:

```text
ControlNet Unit 0
```

Enable:

```text
☑ Enable
```

Optional:

```text
☑ Pixel Perfect
```

---

## Step 2 — Upload Image

Under:

```text
Single Image
```

upload your source image.

Example:

```text
photo.jpg
```

---

## Step 3 — Select Control Type

Choose the control type matching your model.

### Canny

```text
Control Type → Canny
```

### Depth

```text
Control Type → Depth
```

### OpenPose

```text
Control Type → OpenPose
```

### Lineart

```text
Control Type → Lineart
```

### SoftEdge

```text
Control Type → SoftEdge
```

---

# 2️⃣0️⃣ ControlNet Preprocessor

After selecting the Control Type, WebUI should provide the appropriate preprocessor.

Example:

```text
Control Type:
Canny

Preprocessor:
canny

Model:
control_v11p_sd15_canny
```

For Depth:

```text
Control Type:
Depth

Preprocessor:
depth

Model:
control_v11f1p_sd15_depth
```

For OpenPose:

```text
Control Type:
OpenPose

Preprocessor:
openpose

Model:
control_v11p_sd15_openpose
```

---

# 2️⃣1️⃣ Control Weight

Start with:

```text
Control Weight: 1.0
```

If ControlNet is too strong:

```text
0.5 – 0.8
```

If the generated image does not follow the control image enough:

```text
1.0 – 1.5
```

Do not immediately push the value extremely high.

---

# 2️⃣2️⃣ Starting / Ending Control Step

Recommended starting values:

```text
Starting Control Step: 0
Ending Control Step: 1
```

This means ControlNet influences the complete generation process.

Later you can experiment with:

```text
Starting: 0.0
Ending: 0.7
```

or:

```text
Starting: 0.2
Ending: 0.8
```

---

# 2️⃣3️⃣ Control Mode

You will see:

```text
Balanced
My prompt is more important
ControlNet is more important
```

### Recommended

Start with:

```text
Balanced
```

Use:

```text
My prompt is more important
```

when the prompt should have more freedom.

Use:

```text
ControlNet is more important
```

when preserving the source structure is the priority.

---

# 2️⃣4️⃣ SD 1.5 vs SDXL — IMPORTANT

Do not mix these models incorrectly.

### SD 1.5

Use:

```text
v1-5-pruned-emaonly.safetensors
```

with:

```text
control_v11p_sd15_canny.pth
control_v11f1p_sd15_depth.pth
control_v11p_sd15_lineart.pth
control_v11p_sd15_openpose.pth
control_v11p_sd15_softedge.pth
```

### SDXL

Use:

```text
dreamshaperXL_lightningDPMSDE_282807.safetensors
```

or:

```text
juggernautXL_ragnarok_1659952.safetensors
```

with compatible **SDXL ControlNet** models.

Do not select an SD1.5 ControlNet model for an SDXL checkpoint.

---

# 2️⃣5️⃣ CivitAI Browser+

The extension is included here:

```text
extensions\sd-civitai-browser-plus\
```

After starting WebUI, look for:

```text
CivitAI Browser+
```

The extension can be used to browse and download models.

### CivitAI

[![OPEN CIVITAI](https://img.shields.io/badge/🌐%20OPEN-CIVITAI-purple?style=for-the-badge)](https://civitai.com/)

---

# 2️⃣6️⃣ VAE

VAE files go here:

```text
models\VAE\
```

Example:

```text
models/
└── VAE/
    └── your-vae.safetensors
```

Some of the checkpoints used in this setup already include VAE information.

If the checkpoint provides an integrated VAE, you may not need a separate VAE.

---

# 2️⃣7️⃣ Exact Model Checklist

Your original setup contained these files:

## Stable Diffusion

```text
models/Stable-diffusion/

├── v1-5-pruned-emaonly.safetensors
├── realisticVisionV60B1_v51HyperVAE_418901.safetensors
├── dreamshaperXL_lightningDPMSDE_282807.safetensors
└── juggernautXL_ragnarok_1659952.safetensors
```

## ControlNet

```text
models/ControlNet/

├── control_v11p_sd15_canny.pth
├── control_v11f1p_sd15_depth.pth
├── control_v11p_sd15_lineart.pth
├── control_v11p_sd15_openpose.pth
├── control_v11p_sd15_softedge.pth
├── diffusers_xl_canny_mid.safetensors
└── diffusers_xl_depth_mid.safetensors
```

## Extensions

```text
extensions/

├── sd-webui-controlnet/
└── sd-civitai-browser-plus/
```

---

# 2️⃣8️⃣ Verify Everything

Run these commands from the WebUI directory.

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

Expected:

```text
2.1.2+cu121
True
```

### MediaPipe

```powershell
.\venv\Scripts\python.exe -c "import mediapipe as mp; print(mp.__version__); print(hasattr(mp,'solutions'))"
```

Your working setup should report a MediaPipe version with:

```text
solutions: True
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

# 2️⃣9️⃣ Final WebUI Verification

At the bottom of WebUI, verify the environment.

You should see approximately:

```text
version: v1.10.1
python: 3.10.6
torch: 2.1.2+cu121
gradio: 3.41.2
```

Then verify:

```text
✓ Checkpoint appears
✓ Generate works
✓ ControlNet appears
✓ Canny model appears
✓ Depth model appears
✓ OpenPose model appears
✓ Lineart model appears
✓ SoftEdge model appears
✓ SDXL checkpoint appears
✓ CivitAI Browser+ appears
```

---

# 3️⃣0️⃣ First ControlNet Test

Use this simple test before changing advanced settings.

### Checkpoint

Select:

```text
v1-5-pruned-emaonly.safetensors
```

### ControlNet

Enable:

```text
ControlNet Unit 0
```

Upload a normal photograph.

Select:

```text
Control Type → Canny
```

Set:

```text
Preprocessor → Canny
Model → control_v11p_sd15_canny
Control Weight → 1.0
Starting Control Step → 0
Ending Control Step → 1
Control Mode → Balanced
```

Then generate.

If the generated image follows the major edges/composition of the input, ControlNet is working.

---

# 3️⃣1️⃣ Recommended First Settings

For SD 1.5:

```text
Width:        512
Height:       512
Steps:        20–30
CFG Scale:    6–8
Batch Size:   1
Control Weight: 1.0
```

For SDXL:

```text
Width:        1024
Height:       1024
Batch Size:   1
```

SDXL generally requires considerably more VRAM than SD 1.5.

---

# 3️⃣2️⃣ If Generation Is Slow

The biggest factors are:

```text
Resolution
Sampling steps
Model type
ControlNet
Hires. fix
Batch size
```

For a faster test:

```text
512 × 512
20 steps
Batch size 1
Hires. fix OFF
One ControlNet unit
```

Once generation works correctly, increase quality/settings gradually.

---

# 3️⃣3️⃣ Troubleshooting

## ControlNet is visible but models are missing

Check:

```text
models\ControlNet\
```

Then restart WebUI.

---

## Model appears but ControlNet gives an error

Check whether the checkpoint and ControlNet model belong to the same model family.

For example:

```text
SD 1.5 checkpoint
        ↓
SD 1.5 ControlNet
```

and:

```text
SDXL checkpoint
        ↓
SDXL ControlNet
```

Do not mix them.

---

## Python error

Run:

```powershell
.\venv\Scripts\python.exe --version
```

It should be:

```text
Python 3.10.6
```

---

## WebUI environment becomes corrupted

Close WebUI.

Remove:

```text
venv/
repositories/
```

Then start again:

```powershell
.\webui-user.bat
```

WebUI can recreate the environment.

---

# 3️⃣4️⃣ Important Storage Information

The complete working environment can require **tens of gigabytes**.

Models are intentionally not stored in GitHub.

For this setup, the model collection alone can consume many GB:

```text
Stable Diffusion checkpoints
        +
ControlNet models
        +
VAE
        +
Python environment
```

Therefore:

```text
GitHub
  ↓
Source + Extensions + Configuration

Local PC
  ↓
Python environment + Models
```

This is intentional.

---

# 3️⃣5️⃣ Daily Launch

Once everything is installed, you don't need to repeat the setup.

Simply:

```powershell
cd C:\stable-diffusion-webui-setup
.\webui-user.bat
```

Then open the local URL shown in the terminal.

---

# ✅ Complete Setup Checklist

```text
SYSTEM
[ ] Windows 10/11
[ ] NVIDIA driver installed
[ ] nvidia-smi works

PYTHON
[ ] Python 3.10.6 installed
[ ] Python 3.10.6 verified

GIT
[ ] Git installed
[ ] Repository cloned

WEBUI
[ ] WebUI v1.10.1 starts
[ ] PyTorch 2.1.2+cu121
[ ] Gradio 3.41.2

CHECKPOINTS
[ ] v1-5-pruned-emaonly.safetensors
[ ] Realistic Vision V6
[ ] DreamShaper XL Lightning
[ ] Juggernaut XL Ragnarok

CONTROLNET
[ ] Canny
[ ] Depth
[ ] OpenPose
[ ] Lineart
[ ] SoftEdge
[ ] SDXL Canny
[ ] SDXL Depth

EXTENSIONS
[ ] ControlNet v1.1.455
[ ] CivitAI Browser+

TEST
[ ] SD 1.5 generation works
[ ] SDXL generation works
[ ] Canny works
[ ] Depth works
[ ] OpenPose works
[ ] Lineart works
[ ] SoftEdge works
```

---

# 🔗 Official Resources

### AUTOMATIC1111

[![AUTOMATIC1111](https://img.shields.io/badge/Official-AUTOMATIC1111-black?style=for-the-badge)](https://github.com/AUTOMATIC1111/stable-diffusion-webui)

### ControlNet

[![CONTROLNET](https://img.shields.io/badge/Official-ControlNet-blue?style=for-the-badge)](https://github.com/Mikubill/sd-webui-controlnet)

### ControlNet Models

[![CONTROLNET MODELS](https://img.shields.io/badge/ControlNet-Models-blue?style=for-the-badge)](https://huggingface.co/lllyasviel/ControlNet)

### Hugging Face

[![HUGGING FACE](https://img.shields.io/badge/Hugging%20Face-Models-yellow?style=for-the-badge)](https://huggingface.co/models)

### CivitAI

[![CIVITAI](https://img.shields.io/badge/CivitAI-Models-purple?style=for-the-badge)](https://civitai.com/)

### Python 3.10.6

[![PYTHON](https://img.shields.io/badge/Python-3.10.6-blue?style=for-the-badge)](https://www.python.org/downloads/release/python-3106/)

---

## Repository

[![GITHUB](https://img.shields.io/badge/GitHub-oxanuragofficial-black?style=for-the-badge\&logo=github)](https://github.com/oxanuragofficial/stable-diffusion-webui-setup)

---

**Python 3.10.6 → Clone → Launch → Add Models → Configure ControlNet → Generate**




