# 🖥️ Python GUI Application Generator
*A modular, AI-ready template for creating production-quality Python GUI applications.*

---

### **Metadata**
- **Version:** 1.0.0
- **Author:** AI
- **Tags:** python, gui, project-generator, ui, desktop, web, modular

---

### **How to Use**
1.  **Fill in the sections** sequentially.
2.  **Provide your input** where prompted (e.g., "Your turn").
3.  **Type "continue"** to proceed to the next section.
4.  The generator will adapt based on your choices.

---

## 1. Project Overview
**Describe your application in 1-2 sentences.**
*Example: "A desktop and web GUI for image annotation."*

**Your turn:**
> *Your project description here*

---

## 2. Essential Project Details
**Fill in the key details for your project.**
- **Main Goal:** (e.g., "GUI for image annotation")
- **GUI Framework:** (e.g., Gradio, CustomTkinter, PyQt)
- **Target Platforms:** (e.g., Windows, Linux, macOS, Web)
- **Key Dependencies:** (e.g., gradio, customtkinter, Pillow)
- **Testing Framework:** (e.g., pytest)
- **Linting & Formatting:** (e.g., ruff, black)
- **Documentation:** (e.g., MkDocs)
- **CI/CD:** (e.g., GitHub Actions)
- **License:** (e.g., MIT)
- **Author:** (e.g., "Jane Doe")

**Your turn:**
> *Your project details here*

---

## 3. Project Structure
**A project structure will be suggested based on your inputs. Review and request changes.**
*Example Structure:*
```
your_gui_app/
├── src/
│   └── your_gui_app/
│       ├── __init__.py
│       ├── main.py
│       ├── core/
│       │   └── image_processor.py
│       └── gui/
│           ├── web_ui.py
│           └── desktop_ui.py
├── tests/
│   └── test_image_processor.py
├── docs/
│   └── index.md
├── .gitignore
├── pyproject.toml
├── README.md
└── LICENSE
```

**Your turn:**
> *Request any changes to the structure, or type "continue".*

---

## 4. Final Review
**Review the generated configuration and files one last time before completion.**
- [ ] Project overview and details are correct.
- [ ] Project structure is finalized.
- [ ] Build, dependency, and tooling configurations are confirmed.
- [ ] CI/CD workflow is ready.

**Your turn:**
> *Type "done" to complete the generation process.*

---

## 5. Next Steps
- Implement the core logic in the `src/your_gui_app/core` directory.
- Develop the GUI in the `src/your_gui_app/gui` directory.
- Write comprehensive tests in the `tests` directory.
- Update the documentation in the `docs` directory.
- Push your initial commit to trigger the CI/CD pipeline.
