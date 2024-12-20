# ilo_auto

ilo_auto is a Python tool for generating hardware health check reports from ILOM (Integrated Lights-Out Manager). It provides an easy-to-use interface for retrieving system information and generating reports for various hardware nodes. IP of the nodes would be collected from ilo_inventory file. I have shared an example inventory file. Pleae place it under `C:\Users\{your_user_name}\`

## Features

- Supports multiple node types as commandline argument (`WEB`, `DB`, `LOG`).
- Provides a simple command-line tool for generating reports.
- Easy installation and configuration.

## Installation

1. Download and install python from https://www.python.org/ ensuring that you check "Add Python to PATH" during installation. (If not installed already)
2. Download Git for windows https://git-scm.com/downloads/win
3. Create tmp directory under `C:\Users\{your_user_name}\Desktop\`
4. Open Powershell
```powershell
cd C:\Users\{your_user_name}\Downloads\
git clone https://github.com/s41k47/ilo_auto.git
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

# Troubleshooting
Windows Security may create trouble. To solve this
- Create exclusion of `C:\Users\{your_user_name}\AppData\Local\Programs\Python\Python312\Scripts` (Python312 may vary depending on your python version)
- Then try again
