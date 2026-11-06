# Aurelius OS — Debian 12 (Aurelius Edition)

Automated GitHub Actions repository to compile the bootable ISO for **Aurelius OS**.

## What is Aurelius OS?
A hardened, creative-focused Debian 12 ("Bookworm") distribution featuring:
- **Windows-Style Desktop Environment**: Intuitive taskbar, start menu, and dark theme.
- **Zero-Trust Port Lockdown**: UFW firewall blocks all 65,535 incoming ports by default.
- **Creative Suite Pre-Installed**: Spotify, GIMP 2.10, Inkscape, Krita, Blender 3D, Audacity, and 16 art apps.
- **Full Hardware Compatibility**: Peripheral drivers for Wacom tablets, audio DACs, CUPS printing, and Wi-Fi.

## How to Compile the ISO with GitHub Actions:
1. Create a new GitHub repository (e.g. `aurelius-os`).
2. Upload the contents of this repository (`.github/workflows/build-iso.yml`, `build-aurelius-custom-iso.sh`, `README.md`).
3. Push to `main` or open the **Actions** tab and click **Run workflow**.
4. GitHub's cloud servers compile the 3.5 GB bootable `.iso` for free in ~12 minutes.
5. Once finished, download **`aurelius-os-12-amd64.hybrid.iso`** from the workflow run's **Artifacts**!

## How to Flash to USB:
- Windows: Use [Rufus](https://rufus.ie) in ISO Hybrid mode.
- Mac / Linux: Use [Ventoy](https://www.ventoy.net) or `sudo dd if=aurelius-os-12-amd64.hybrid.iso of=/dev/sdX bs=4M status=progress`.
