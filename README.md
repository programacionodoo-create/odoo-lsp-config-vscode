# Practical Guide: OdooLS in VSCode for Odoo

Welcome to the **OdooLS VSCode Setup Guide**. This repository provides step-by-step instructions and reference configurations to set up **Odoo Language Server (OdooLS)** for Visual Studio Code, enabling full Python and XML autocompletion, go-to-definition, and workspace diagnostics.

---

> [!NOTE]
> **Do you need to clone this repository?**
> 
> No! This repository is designed as a reference guide and configuration template. You do not need to clone the entire setup—simply select your Operating System below, follow the steps, and copy the relevant configuration files (`odools.toml`, `pyrightconfig.json`) into your Odoo project root.

---

## 🔀 Select Your Operating System

Follow the dedicated guide according to your development environment:

| Branch / Guide | Target System | Terminal Shell | Pathing Style |
| :--- | :--- | :--- | :--- |
| 🪟 **[Windows Guide](../../tree/windows)** | Windows 10 / 11 | `CMD` / `PowerShell` | `C:\Users\...\` |
| 🐧 **[Linux / macOS Guide](../../tree/linux)** | Ubuntu, Debian, macOS | `Bash` / `Zsh` | `~/dev/...` |

---

## Features in Action

![Python Autocompletion](assets/completion_python.png)

---

## Overview of Key Configuration Files

Regardless of your Operating System, setting up OdooLS revolves around two primary configuration files placed at the root of your custom addons workspace:

### 1. `odools.toml`
Defines the environment pathways for the Odoo Language Server extension:
* `odoo_path`: Points to your local Odoo core source code repository.
* `python_path`: Points to the Python interpreter inside your dedicated virtual environment.
* `addons_paths`: Array of custom, OCA, or Enterprise module directories.

### 2. `pyrightconfig.json`
Provides general Python language diagnostics and type checking resolution via Pyright / Pylance, preventing false positive import errors for Odoo modules.

---

## 📁 Recommended Workspace Structure

```text
my-odoo-project/
├── .vscode/
├── odools.toml          
├── pyrightconfig.json   
├── addons/             
├── enterprise/         
└── oca/                 