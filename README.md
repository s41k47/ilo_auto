# ilo_auto

ilo_auto is a Python tool for generating hardware health check reports from ILOM (Integrated Lights-Out Manager). It provides an easy-to-use interface for retrieving system information and generating reports for various hardware nodes. __IP of the nodes would be collected from ilo_inventory file. I have shared an example inventory file. Pleae place it under C:\Users\{your_user_name}\ __

## Features

- Supports multiple node types as commandline argument (`WEB`, `DB`, `LOG`).
- Provides a simple command-line tool for generating reports.
- Easy installation and configuration.

## Installation

# On Linux
1. Make sure you have python3, python3-pip and git installed
```bash
sudo dnf update
sudo dnf install -y git python3 python3-pip
```

2. Clone and install using pip
```bash
cd ~/Downloads
git clone <repository_url>
cd cd ~/Downloads/ilo_auto
pip install .
```

# On Windows
1. Download and install python from https://www.python.org/ ensuring that you check "Add Python to PATH" during installation. (If not installed already)
2. Download Git for windows https://git-scm.com/downloads/win
3. Create tmp directory under C:\Users\{your_user_name}\Desktop\
4. Open Powershell
```powershell
cd C:\Users\{your_user_name}\Downloads\
git clone <repository_url>
cd ilo_auto
pip install -e .
```

## Verify installation
```bash
hcilo --help
or
pip show ilo_auto
```

## Usage
- To generate report for all nodes
```bash
hcilo --all
```

- To generate report for a single node group. (example: for WEB)
```bash
hcilo WEB
```

- To generate report for a multiple node group. (example: for WEB and DB)
```bash
hcilo WEB DB
```