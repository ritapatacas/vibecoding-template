# 🪟 Windows Setup

## Setup Steps

### Step 1: Python

> Check if Python is installed:

```powershell
python --version
```

**Errors like "Python is not recognized":**

> **Method 1:** Install Python using PowerShell - open the terminal and run:

```powershell
winget install Python.Python.3.13
```

> **Method 2:** Manual download

1. Go to <https://www.python.org/downloads/>
2. Download and run the installer
3. **Important:** Check the box "Add Python to PATH" during installation

### Step 2: Create Virtual Environment

> Create a virtual environment

```powershell
python -m venv .venv
```

> Activate the environment (everytime you don't see `( .venv )` in the terminal)

```powershell
.venv\Scripts\activate
```

> Upgrade pip

```powershell
python -m pip install --upgrade pip
```

**Errors like "running scripts is disabled on this system":**

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

**Errors like "developer tools not found"**

```powershell
pip install --upgrade pip setuptools wheel
```

## Install Packages

> Install libraries (run this everytime you add new packages)

```powershell
pip install -r requirements.txt
```

> Or just install a specific one

```powershell
pip install <package_name>
```
