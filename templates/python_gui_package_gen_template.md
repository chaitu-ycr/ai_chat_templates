🖥️ **Python GUI Application Package Creation Template (AI-Ready, Step-by-Step)**

---

# 1️⃣ Project Overview

**Describe your application in 1-2 sentences.**  
*Example:*  
> "A desktop and web GUI for image annotation with automated testing and CI/CD integration."

**Please provide your project overview.**  
*Type your answer, then say "continue" to proceed.*

---

# 2️⃣ Essential Project Details

**Fill in each point below. Example answers are provided.**

- **Main goal:** (e.g., "Desktop GUI for image annotation")
- **GUI type:** (Web [Gradio], Desktop [CustomTkinter], or both)
- **Execution environment:** (local, CI/CD, Docker, cloud)
- **Key dependencies:** (e.g., gradio, customtkinter, pytest)
- **Testing needs:** (unit, integration, E2E)
- **Code style/linting:** (e.g., black, ruff, mypy)
- **Documentation:** (e.g., mkdocs, pdoc)
- **CI/CD integration:** (e.g., GitHub Actions)
- **License & author:** (e.g., MIT, Author: Alex Smith)

**Please fill in your project details above.**  
*Type your answers, then say "continue" to proceed.*

---

# 3️⃣ Recommended Setup

**Review the recommended setup. Example:**

- **Package Manager:** uv
- **Python Version:** 3.12
- **Standards:** PEP 8, PEP 621, PEP 517
- **Type Hints & Docstrings:** Yes
- **Testing:** pytest, 100% coverage
- **Pre-commit Hooks:** Yes
- **Modular Design:** Yes

**Please confirm or modify your setup.**  
*Type your preferences, then say "continue" to proceed.*

---

# 4️⃣ Project Structure

**Suggested layout (edit as needed):**
```
your_gui_app/
├── src/
│   └── your_gui_app/
│       ├── __init__.py
│       ├── main.py
│       ├── core/
│       │   ├── processor.py
│       │   └── utils.py
│       ├── gui/
│       │   ├── web_interface.py       # Gradio
│       │   └── desktop_interface.py   # CustomTkinter
│       └── config/
│           └── settings.py
├── tests/
│   └── test_processor.py
├── pyproject.toml
├── README.md
├── LICENSE
└── .gitignore
```
**Please confirm or suggest changes to your desired structure.**  
*Type your answer, then say "continue" to proceed.*

---

# 5️⃣ `pyproject.toml` Configuration

**Example configuration:**
```toml
[project]
name = "your-gui-app"
version = "0.1.0"
description = "A Python GUI application package"
authors = [{ name = "Your Name", email = "you@example.com" }]
license = "MIT"
readme = "README.md"
requires-python = ">=3.10"

dependencies = [
    "pytest",
    "gradio",
    "customtkinter",
    "typing-extensions"
]

[project.optional-dependencies]
dev = [
    "black",
    "ruff",
    "mypy",
    "pytest-cov",
    "pre-commit"
]

[tool.black]
line-length = 88
target-version = ["py310"]

[tool.ruff]
line-length = 88
select = ["E", "F", "I"]
ignore = ["E501"]

[tool.mypy]
strict = true

[build-system]
requires = ["uv"]
build-backend = "uv.build"
```
**Please fill in or confirm your project metadata.**  
*Type your answer, then say "continue" to proceed.*

---

# 6️⃣ CI/CD Workflow (GitHub Actions)

**Example workflow:**
```yaml
name: GUI Application CI
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v3
    - name: Set up Python
      uses: actions/setup-python@v4
      with:
        python-version: '3.12'
    - name: Install uv
      run: |
        curl -LsSf https://astral.sh/uv/install.sh | sh
    - name: Install dependencies
      run: uv pip install -r requirements.txt
    - name: Run tests
      run: pytest --cov=src
    - name: Check formatting
      run: black --check src tests
    - name: Lint code
      run: ruff check src tests
    - name: Type check
      run: mypy src
```
**Please confirm or adapt the workflow for your needs.**  
*Type your answer, then say "continue" to proceed.*

---

# 7️⃣ Documentation Tooling

**Choose your preferred tool. Example:**

- **MkDocs:**  
  - Install: `uv pip install mkdocs mkdocs-material`  
  - Init: `mkdocs new docs`  
  - Edit `mkdocs.yml` as needed

- **pdoc:**  
  - Install: `uv pip install pdoc`  
  - Generate: `pdoc src/your_gui_app --html --output-dir docs`

**Please select and confirm your documentation tool.**  
*Type your answer, then say "continue" to proceed.*

---

# 8️⃣ Final Checklist

- [ ] Project overview and details filled
- [ ] Setup confirmed
- [ ] Structure reviewed
- [ ] `pyproject.toml` customized
- [ ] CI/CD workflow ready
- [ ] Documentation tool chosen
- [ ] Code runnable out-of-the-box
- [ ] Tests and linting pass

**Please review the checklist and confirm completion.**  
*Type "done" when finished.*
