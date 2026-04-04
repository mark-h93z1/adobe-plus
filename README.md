# 📦 adobe-plus

![License](https://img.shields.io/github/license/mark-h93z1/adobe-plus) ![Stable](https://img.shields.io/badge/status-stable-brightgreen.svg)

[![tool](https://img.shields.io/badge/tool-MIT-green?style=flat-square) ![Version](https://img.shields.io/badge/Version-1.2.0-blue?style=flat-square) ![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square) ![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white) ![Stars](https://img.shields.io/github/stars/mark-h93z1/adobe-plus?style=flat-square) ![Last Commit](https://img.shields.io/github/last-commit/mark-h93z1/adobe-plus?style=flat-square)

Windows Adobe config tool with profile mgmt

## 📥 Download

[![Download Latest](https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge&logo=github)](../../releases/latest)

1. Download the latest release from the link above
2. Extract the archive (WinRAR / 7-Zip)
3. Run `python main.py` (or see Usage below)
4. Configure settings in `config.yaml`

## FAQ

<details>
 <summary>What Adobe products are supported?</summary>
 Currently, Photoshop, Illustor, and Premiere Pro are supported. More to come.
</details>

<details>
 <summary>How do I create a new profile?</summary>
 Edit the `config.yaml` file and add a new profile under the `profiles` section. Then, restart the tool.
</details>

<details>
 <summary>Can I run multiple profiles at the same time?</summary>
 No, the tool only supports running one profile at a time.
</details>

## Requirements

Make sure you have Python 3.11 or higher installed.

These Python packages are needed:

* `PyYAML`
* `psutil`
* `requests`
* `Pillow`

Install them via pip:

```bash
pip install -r requirements.txt
```

## Troubleshooting

* **Tool doesn't start:** Make sure you have Python 3.11+ installed.
* ** fails:** Set the `adobe_path` manually in `config.yaml`. Double-check the path.
* **Profile isn't loading:** Verify the profile name in `config.yaml` matches the one you selected in the GUI. Also, check for YAML syntax errors (use a YAML validator).
* **GUI issues:** Try running the tool with admin privileges.

## Config

The `config.yaml` file controls the tool's behavior. Here's an example:

```yaml
adobe_path: "C:\\Program Files\\Adobe\\Adobe Photoshop 2024"
profile_directory: "profiles"
auto_detect: true

profiles:
 default:
 settings:
 performance:
 memory_usage: 70
 scch_disks:
 - "D:\\temp"
 - "E:\\temp"
 interface:
 ui_scaling: 100
 recent_files: 20
 photo_editing:
 settings:
 performance:
 memory_usage: 80
 scch_disks:
 - "F:\\temp"
 interface:
 ui_scaling: 125
 recent_files: 10
```

`adobe_path`: The main Adobe install folder. Leave blank for .

`profile_directory`: Where profile files are stored.

`auto_detect`: If true, it tries to find the path automatically.

Each profile has a name (e.g., `default`, `photo_editing`) and settings.

## Getting Started

To run the tool:

```bash
python main.py
```

It auto-detects the Adobe install path. If it fails, you can manually set it in `config.yaml`.

## Highlights

This tool offers the following features:

* It's a full version with all features enabled. No registion required.
* finds the Adobe installation path.
* It's portable – no installation needed, just run the `main.py`.
* Premium features are enabled by default. You get the good stuff.
* Profile management lets you switch between different Adobe configuions.

TODO: Add support for more Adobe products. WIP.

---

🌍 Available in multiple languages — check README_* files
