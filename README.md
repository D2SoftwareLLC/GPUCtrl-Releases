<p align="center">
  <img src="https://gpuctrl.com/assets/icons/logo.svg" alt="GPUCtrl" width="160" />
</p>

<h1 align="center">GPUCtrl</h1>

<p align="center"><strong>Stop fighting your GPUs.</strong></p>

<p align="center">
  <a href="https://gpuctrl.com">Website</a> ·
  <a href="https://github.com/D2SoftwareLLC/GPUCtrl-Releases/releases/latest">Latest release</a> ·
  <a href="https://gpuctrl.com/dashboard">Dashboard</a> ·
  <a href="mailto:gpuctrl@gmail.com">Support</a>
</p>

---

GPUCtrl is a desktop application for managing and launching GPU‑accelerated workloads — Stable Diffusion, LLMs, training pipelines, video encoding — with intelligent GPU routing across NVIDIA and AMD hardware on Windows and Linux.

> This repository hosts **release binaries only**. GPUCtrl is closed‑source commercial software; the source code is not published here. Use of the binaries is governed by the [End User License Agreement](https://gpuctrl.com/terms).

## Download

Get the latest installer from the [**Releases**](https://github.com/D2SoftwareLLC/GPUCtrl-Releases/releases/latest) page, or directly from [gpuctrl.com](https://gpuctrl.com).

| Platform | File | Notes |
| --- | --- | --- |
| Windows 10 / 11 (x64) | `GPUCtrl-Setup.exe` | NSIS installer, recommended |
| Windows 10 / 11 (x64) | `GPUCtrl.msi` | MSI installer, for fleet deployment |
| Linux (AppImage, x86_64) | `GPUCtrl.AppImage` | Portable, works on any modern distro |
| Linux (Debian / Ubuntu, x86_64) | `gpuctrl.deb` | Debian package |

A `SHA256SUMS.txt` is published alongside each release for verification.

## Install

### Windows

1. Download `GPUCtrl-Setup.exe` (or `GPUCtrl.msi`) from the [latest release](https://github.com/D2SoftwareLLC/GPUCtrl-Releases/releases/latest)
2. Run the installer. Windows SmartScreen will show **"Windows protected your PC"** — click **More info → Run anyway**. The Windows build is in beta and not yet code‑signed; a signed installer ships with v1.0
3. Follow the installer prompts. GPUCtrl launches automatically on first install completion

### Linux — Debian / Ubuntu

```bash
sudo apt install ./gpuctrl.deb
```

If apt complains about missing dependencies, run `sudo apt-get install -f` to resolve them.

### Linux — AppImage

Works on any modern x86_64 distribution. No install needed — just make the file executable:

```bash
chmod +x GPUCtrl.AppImage
./GPUCtrl.AppImage
```

To integrate with your application menu, move it to `~/Applications/` and use a tool like [appimaged](https://github.com/probonopd/go-appimage) for desktop registration.

### Verifying your download (optional)

```bash
sha256sum -c SHA256SUMS.txt
```

Run from the directory containing the downloaded artifacts and the `SHA256SUMS.txt` file.

## First launch

GPUCtrl requires a free account to use. On first launch you'll be prompted to sign in.

If you don't have an account yet, **[sign up at gpuctrl.com/signup](https://gpuctrl.com/signup)** — no credit card required. New accounts include a **7‑day trial with full feature access**.

## Getting started

After signing in:

1. **GPUs tab** — confirm GPUCtrl detected your hardware (NVIDIA, AMD, or both). VRAM, utilization, temperature, and NVLink topology surface in real time.
2. **Profiles tab** — click **New profile**, pick an app type (ComfyUI, Stable Diffusion WebUI, Ollama, Blender, vLLM, and 9 more), and assign it to specific GPUs. Use the built‑in argument helper for inline docs on every flag.
3. **Dashboard** — favorite the profile and launch it with one click.

GPUCtrl handles GPU pinning (`CUDA_VISIBLE_DEVICES`, `HIP_VISIBLE_DEVICES`), virtual environment activation, terminal management, and process cleanup automatically.

See [gpuctrl.com](https://gpuctrl.com) for the full feature tour.

## What it does

- Detects every NVIDIA and AMD GPU in the system with VRAM, utilization, temperature, power, and clock metrics
- Launches AI / ML applications (ComfyUI, Automatic1111, Forge, Fooocus, Ollama, vLLM, Text Generation WebUI, Kohya, InvokeAI, LM Studio, Blender, DaVinci Resolve, OBS) with GPU pinning, virtual environment activation, and live process output streaming
- Routes specific workloads to specific GPUs, including NVLink groups and multi‑GPU configurations
- Container‑aware: launches inside Docker, LXD, and systemd‑nspawn with GPU passthrough
- Workflow automation for sequential or parallel multi‑profile launches
- VRAM fragmentation detection, GPU history charts, and a built‑in diagnostics viewer

## Pricing

- **7‑day free trial** — no credit card required, full feature access
- **Pro license** — **$19** one‑time (launch promotion, regular price $39), lifetime updates, two devices

Sign up and start the trial at [gpuctrl.com/signup](https://gpuctrl.com/signup).

## License

GPUCtrl is proprietary, closed‑source commercial software. See the [LICENSE](./LICENSE) file in this repository for the full notice, and the [End User License Agreement](https://gpuctrl.com/terms) for the binding terms that apply when you install or run GPUCtrl.

Open‑source components bundled with GPUCtrl are listed inside the application under **About → Open Source Licenses**, with full attribution and license texts.

## Support

- **Account, billing, license issues:** [gpuctrl.com/dashboard](https://gpuctrl.com/dashboard)
- **General support:** gpuctrl@gmail.com
- **Installation problems with a specific release:** open an issue on this repository

## Trust

Each release on this page is published directly by D2 Software LLC via an automated build pipeline. If you obtain a GPUCtrl installer from any source other than this Releases page or [gpuctrl.com](https://gpuctrl.com), **do not run it**.

---

<p align="center">
  © 2026 D2 Software LLC · GPUCtrl is a trademark of D2 Software LLC.
</p>
