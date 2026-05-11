# Viewing the Docs Locally

## Prerequisites
- Python 3.x installed

## Setup

**1. Create a virtual environment**
```bash
python -m venv mkdocs
```

**2. Activate the environment**

On Windows:
```bash
.\mkdocs\Scripts\activate
```

**3. Install MkDocs**
```bash
pip install mkdocs pymdown-extensions
```

**4. Serve the docs**
```bash
mkdocs serve --livereload
```

Open your browser at **http://127.0.0.1:8000**

---

> To stop the server, press `Ctrl+C`. To deactivate the virtual environment, run `deactivate`.