🧪 **Python Package Creation Template for Test Automation (AI-Optimized, Step-by-Step)**

---

# 1️⃣ Project Intent

**Describe your package in 1-2 sentences.**  
*Example:*  
> "Automated API testing for RESTful services in CI/CD pipelines."

**Please provide your project intent before continuing.**  
---

# 2️⃣ Essential Project Details

**Fill in each point below. Example answers are provided.**

- **Main goal:** (e.g., API testing, UI automation, data validation)
- **Execution environment:** (CI/CD, Docker, cloud, local dev)
- **Key dependencies:** (e.g., pytest, requests, selenium)
- **Testing needs:** (unit, integration, E2E)
- **Code style/linting:** (e.g., black, ruff, mypy)
- **Documentation:** (e.g., mkdocs, pdoc)
- **CI/CD integration:** (e.g., GitHub Actions)
- **License & author:** (e.g., MIT, Jane Doe)

*Example:*  
> Main goal: API testing for a RESTful service  
> Runs in: CI/CD (GitHub Actions) and local dev  
> Libraries: pytest, requests  
> Tests: unit and integration  
> Style: black, ruff, mypy  
> Docs: mkdocs  
> CI/CD: Yes, GitHub Actions  
> License: MIT, Author: Jane Doe

**Please provide your project details above before continuing.**  
---

# 3️⃣ Recommended Setup

**Review and confirm or modify the recommended setup. Example:**  
- **Package Manager:** uv  
- **Python Version:** 3.12  
- **Standards:** PEP 8, PEP 621, PEP 517  
- **Type Hints & Docstrings:** Yes  
- **Testing:** pytest, 100% coverage  
- **Pre-commit Hooks:** Yes  
- **Modular Design:** Yes  

**Please confirm or edit your setup before proceeding.**  
---

# 4️⃣ Project Structure

**Suggested layout (edit as needed):**
```
your_package/
├── src/
│   └── your_package/
│       ├── __init__.py
│       ├── core.py
│       └── utils.py
├── tests/
│   ├── __init__.py
│   ├── test_core.py
│   └── test_utils.py
├── .gitignore
├── pyproject.toml
├── README.md
├── LICENSE
└── .pre-commit-config.yaml
```
**Please confirm or suggest changes to your desired structure before continuing.**  
---

# 5️⃣ `pyproject.toml` Configuration

**Example configuration:**
```toml
[project]
name = "your-package-name"
version = "0.1.0"
description = "A Python package for test automation"
authors = [{ name = "Your Name", email = "you@example.com" }]
license = "MIT"
readme = "README.md"
requires-python = ">=3.10"

dependencies = [
    "pytest",
    "requests",
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
**Please fill in or confirm your project metadata before continuing.**  
---

# 6️⃣ CI/CD Workflow (GitHub Actions)

**Example workflow:**
```yaml
name: Test Automation Workflow
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
**Please confirm or adapt the workflow above for your needs before continuing.**  
---

# 7️⃣ Documentation Tooling

**Choose your preferred tool. Example:**  
- **MkDocs:**  
  - Install: `uv pip install mkdocs mkdocs-material`  
  - Init: `mkdocs new docs`  
  - Edit `mkdocs.yml` as needed  
- **pdoc:**  
  - Install: `uv pip install pdoc`  
  - Generate: `pdoc src/your_package --html --output-dir docs`  

**Please select and confirm your documentation tool before continuing.**  
---

# 8️⃣ Final Checklist

- [ ] Structure and code reviewed
- [ ] Modifications/additions confirmed
- [ ] Code runnable out-of-the-box
- [ ] Test results displayed
- [ ] Improvements suggested

**Please review the checklist and confirm completion.**  
*Type "done" when finished.*
