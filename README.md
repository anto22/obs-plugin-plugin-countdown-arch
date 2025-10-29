# obs-plugin-plugin-countdown-arch

![OBS Plugin Countdown Installer](https://img.shields.io/badge/OBS_Plugin-Countdown-blue?logo=obsstudio&logoColor=white&style=for-the-badge)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Arch_Linux-blue.svg)](#)
[![Language](https://img.shields.io/badge/language-Bash-orange.svg)](#)
[![Status](https://img.shields.io/badge/status-Stable-brightgreen.svg)](#)
[![OBS](https://img.shields.io/badge/OBS-Plugin-black.svg)](https://obsproject.com)

---

## 🧠 Overview

This script automatically installs the **OBS Countdown Plugin** on **Arch Linux**  
and derivatives (like Manjaro, EndeavourOS, Garuda, etc.).

No manual compilation, no AUR helper required — just run and it handles everything  
(using `pacman` or `yay` when available).

---

## 🚀 Features

✅ Installs the official *OBS Countdown Plugin* for Arch-based systems  
✅ Checks and installs dependencies automatically  
✅ Works on both native Arch and Manjaro  
✅ Lightweight: a single Bash script  
✅ Perfect for OBS streamers who want a simple timer overlay ⏱️  

---

## 🧩 Usage

Clone this repository and execute the script:

```bash
sudo pacman -S --needed base-devel git

# 2) Récupérer le PKGBUILD
git clone https://github.com/anto22/obs-plugin-plugin-countdown-arch.git
cd obs-plugin-plugin-countdown-arch

# 3) Construire et installer
makepkg -si
