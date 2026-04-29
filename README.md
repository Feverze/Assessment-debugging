# Assessment Debugging

This is a Dash-based assessment project.
Follow the steps below to run the app on Fedora Linux without modifying the system Python environment.

---

## Setup Instructions

### Platform choice
Use either **Arch Linux** or **Fedora Linux**.  
The instructions below use **Fedora Linux**.

### 1. Install system dependencies (Fedora)
Install Git and curl only:

```
sudo dnf install -y git curl
```

### 2. Install `uv` (modern package manager)

```
curl -LsSf https://astral.sh/uv/install.sh | sh
source "$HOME/.local/bin/env"
```

`uv` respects both `pyproject.toml` and `.python-version`.

### 3. Clone the repository

```
git clone https://github.com/osamaegy/Assessment-debugging.git
cd Assessment-debugging
```

### 4. Create and activate a project virtual environment
Do not install dependencies into system Python.

```
uv venv --python 3.12
source .venv/bin/activate
```

### 5. Install project dependencies from `pyproject.toml`

```
uv sync
```

### 6. Run the application

```
python main.py
```

### 7. Open the app in your browser

Open the URL in your browser http://127.0.0.1:10030/ to view it.
