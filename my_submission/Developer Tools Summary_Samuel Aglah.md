# Developer Tools Summary

This document provides a summary of three important tools commonly used in modern development and data science workflows:

- Visual Studio Code (VS Code)
- UV Package Manager
- Plotly Visualization Library

---

# 1. Visual Studio Code (VS Code)

**Visual Studio Code (VS Code)** is a free and powerful code editor developed by Microsoft. It is widely used for writing, debugging, and managing code across many programming languages.

## Key Features

- **Multi-language support** (Python, JavaScript, HTML, CSS, etc.)
- **IntelliSense** for smart autocomplete and code suggestions
- **Integrated terminal** to run commands inside the editor
- **Git integration** for version control
- **Extensions marketplace** for adding additional functionality
- **Customizable interface** with themes and settings

## Important Sections of VS Code

- **Activity Bar** – Access Explorer, Search, Git, Debug, and Extensions
- **Editor Area** – Where code files are opened and edited
- **Terminal** – Run commands directly inside VS Code

## Useful Shortcuts

| Shortcut | Action |
|--------|--------|
| Ctrl/Cmd + Shift + P | Command Palette |
| Ctrl/Cmd + P | Quick file search |
| Ctrl/Cmd + F | Find text |
| Ctrl + ` | Open terminal |

## Why Developers Use VS Code

VS Code is lightweight, fast, highly customizable, and supports thousands of extensions, making it one of the most popular development environments.

---

# 2. UV Package Manager

**UV** is a modern Python package manager written in Rust. It is designed to be extremely fast and replaces traditional tools like `pip`, `venv`, and `pyenv`.

## Key Advantages

- **10–100× faster than pip**
- Automatic **virtual environment management**
- Reliable **dependency resolution**
- Simplifies Python project setup

## Common Commands

### Create a Project
```bash
uv init project-name
```

### Install Dependencies
```bash
uv sync
```

### Add a Package
```bash
uv add package-name
```

### Remove a Package
```bash
uv remove package-name
```

### Run Python Script
```bash
uv run python script.py
```

## Project Configuration

UV uses the **`pyproject.toml`** file to manage:

- project metadata
- Python version requirements
- project dependencies

Example dependency list:

```toml
dependencies = [
    "polars",
    "plotly",
    "marimo"
]
```

## Virtual Environments

UV automatically creates a **`.venv` folder** to isolate dependencies, ensuring projects remain clean and reproducible.

---

# 3. Plotly Visualization Library

**Plotly** is a Python library used to create **interactive and visually appealing data visualizations**.

It is widely used in **data science, analytics, dashboards, and reporting**.

## Key Features

- Interactive charts
- Hover tooltips
- Zoom and pan functionality
- Professional styling
- Exportable to HTML or images

## Two Main Plotly Interfaces

### Plotly Express (px)

A simple interface for quickly creating charts.

Example:

```python
import plotly.express as px

fig = px.scatter(df, x="age", y="score")
fig.show()
```

### Graph Objects (go)

Provides more control and customization.

Example:

```python
import plotly.graph_objects as go

fig = go.Figure()
fig.add_trace(go.Scatter(x=[1,2,3], y=[4,5,6]))
fig.show()
```

## Common Chart Types

- Line charts
- Bar charts
- Scatter plots
- Histograms
- Pie charts
- Heatmaps
- Box plots
- 3D visualizations

## Interactive Features

Users can:

- Hover to see data details
- Zoom into charts
- Pan across datasets
- Filter data
- Reset views

## Exporting Charts

Plotly charts can be exported in several formats:

### Interactive HTML
```python
fig.write_html("chart.html")
```

### Image Formats
```python
fig.write_image("chart.png")
```

Supported formats include:

- PNG
- JPG
- SVG
- PDF
- HTML

---

# Conclusion

These tools play important roles in modern development workflows:

| Tool | Purpose |
|-----|------|
| **VS Code** | Writing and managing code |
| **UV** | Managing Python packages and environments |
| **Plotly** | Creating interactive data visualizations |

Together, they help developers and data scientists build efficient, maintainable, and interactive projects.