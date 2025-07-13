# Week 1: Environment Setup & Python Fundamentals | AnimAI Project

Welcome to Week 1, we'll set up our Python development environment, get familiar with basic Python concepts through examples, and learn essential libraries for data analysis.

## Table of Contents
1. [Python & VS Code Installation](#python--vs-code-installation)
2. [Basic Python Introduction](#basic-python-introduction)
3. [Jupyter Notebooks in VS Code](#jupyter-notebooks-in-vs-code)
4. [Essential Libraries](#essential-libraries)
5. [Week 1 Assignment](#week-1-assignment)

## Python & VS Code Installation

Before diving into the project, let's set up a proper development environment:

**Video Tutorial:** [How to Install Python and VS Code](https://www.youtube.com/watch?v=cUAK4x_7thA)

### Installing Python
1. Visit the [official Python website](https://www.python.org/downloads/) and download the latest stable version (3.9+) for your operating system.
2. During installation, make sure to check the box that says "Add Python to PATH" to use Python from any command line.

**Command line verification:**
```bash
python --version  # Check if Python is installed correctly
pip --version     # Verify pip installation
```

### Installing VS Code
VS Code is our recommended editor for this project:

1. Download VS Code from the [official website](https://code.visualstudio.com/download) for your operating system.
2. Install and launch VS Code.
3. Install the Python extension:
   - Go to Extensions (Ctrl+Shift+X or Cmd+Shift+X)
   - Search for "Python"
   - Install the Microsoft Python extension

## Basic Python Introduction

Once your environment is set up, explore the Python example files in the `python-examples` directory. Each file covers important Python concepts and should take approximately 15-20 minutes to understand if you're new to Python.

Work through these examples over 2-3 days to build a solid foundation before moving to the more complex aspects of the AnimAI project.

## Jupyter Notebooks in VS Code

### Why Jupyter Notebooks?
When working on data analysis and AI projects, you'll often want to:
- Run specific parts of your code without executing the entire program
- See results immediately next to your code
- Include documentation and explanations alongside your code
- Share your work with visualizations and comments

Jupyter notebooks (.ipynb files) solve these problems by providing an interactive environment where you can:
- Execute code cells individually
- Add markdown cells for documentation
- Display graphs, images, and tables inline
- Create a narrative flow of your analysis

### Setting Up Jupyter in VS Code

1. Install Jupyter support via pip:
```bash
pip install jupyter notebook ipykernel
```

2. Create a new Jupyter notebook in VS Code:
   - Press Ctrl+Shift+P (or Cmd+Shift+P on Mac)
   - Type "Create: New Jupyter Notebook"
   - Select the Python interpreter when prompted

3. Using Jupyter notebooks:
   - Code cells: Write and execute Python code (Press Shift+Enter to run)
   - Markdown cells: Add formatted text, equations, and explanations
   - Output: View results directly below each cell

**Video Tutorial:** [Setting up and Using Jupyter Notebooks in VS Code](https://www.youtube.com/watch?v=DA6ZAHBPF1U)

## Essential Libraries

For the AnimAI project, we'll be using several core libraries for data analysis and manipulation. Install them using pip:

```bash
pip install numpy pandas matplotlib
```

### NumPy
NumPy is the foundation for numerical computing in Python and will be essential for our AI work.

**Installation verification:**
```python
import numpy as np
print(np.__version__)
```
Run this in a `test.py` file.

**Resources:**
- [W3Schools NumPy Tutorial](https://www.w3schools.com/python/numpy/default.asp)
- [Kaggle NumPy Tutorial](https://www.kaggle.com/code/legendadnan/numpy-tutorial-for-beginners)

Choose any one of the resources, it is recommended that you follow everything by running the code in some `test.py` file so that you can experience for yourself.
### Pandas
Pandas will help us handle and analyze structured data.

**Installation verification:**
```python
import pandas as pd
print(pd.__version__)
```

**Resources:**
- [W3Schools Pandas Tutorial](https://www.w3schools.com/python/pandas/default.asp)
- [Kaggle Pandas Tutorial](https://www.kaggle.com/learn/pandas)

### Matplotlib
Matplotlib allows us to create visualizations of our data and results.

**Installation verification:**
```python
import matplotlib.pyplot as plt
print(plt.__version__)
```

**Resources:**
- [W3Schools Matplotlib Tutorial](https://www.w3schools.com/python/matplotlib_intro.asp)
- [Kaggle Matplotlib Tutorial](https://www.kaggle.com/code/prashant111/matplotlib-tutorial-for-beginners)

## Week 1 Assignment

Please review the `Assignment-01.ipynb` file for your first AnimAI project task. This assignment includes basic data analysis exercises to practice what you've learned about Python, NumPy, Pandas, and Matplotlib.

**Key Assignment Components:**
- Data loading and manipulation with Pandas
- Statistical analysis with NumPy
- Data visualization with Matplotlib
- Documentation of your process in a Jupyter notebook

**Submission Guidelines:**
- Complete the assignment in the same Jupyter notebook `Assignment-01.ipynb` file
- Make sure all code cells run without errors
- Include markdown cells explaining your approach in the `Assignment-01.ipynb` file itself, no need to create separate report

> **Submission Deadline**: **`28th May, 2025`**  
You can submit your work directly through **WhatsApp**, however, we **strongly recommend** maintaining a **GitHub repository** for this project.

This not only ensures version control and professional organization of your code but also significantly enhances your visibility and credibility when showcasing your portfolio for internships, open-source contributions, or academic references. Repositories that reflect structured commits, thoughtful documentation, and clean modular code can serve as powerful assets in both academic and industry settings.

**Make sure your GitHub repo includes:**
- A clear `README.md` explaining the project  
- Well-commented code notebooks or `.py` files  
- A folder structure separating raw data, notebooks, and reports  
- Screenshots or visuals of results wherever applicable

If you need guidance on how to set up a GitHub repo for this, feel free to ask.


## Additional Resources

- [Python Official Documentation](https://docs.python.org/3/)
- [Real Python Tutorials](https://realpython.com/)
- [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)

Good luck with Week 1 of the AnimAI! If you have any questions, don't hesitate to ask us.
