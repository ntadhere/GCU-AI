# Guide: Installing Jupyter Notebook with Miniforge

This guide shows you how to install **Miniforge**, create a Python environment, and run **Jupyter Notebook** from the terminal.

---

## 1. Install Miniforge

Miniforge is a minimal conda installer. It lets you manage Python environments easily.

### macOS / Linux
Open your terminal and run:

```bash
# Download the Miniforge installer (for your system)
curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh   # for Apple Silicon
# or
curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-x86_64.sh # for Intel Macs
# or
curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh  # for Linux

# Give execute permission and run installer
chmod +x Miniforge3-*.sh
./Miniforge3-*.sh
```

Follow the prompts and restart your terminal.

### Windows
1. Download the `.exe` installer from [Miniforge releases](https://github.com/conda-forge/miniforge/releases).
2. Run the installer and follow the setup wizard.
3. Open **"Miniforge Prompt"** from the Start Menu.

---

## 2. Create a New Python Environment

```bash
# Update conda
conda update conda -y

# Create a new environment called "jupyter_env" with Python 3.10
conda create -n jupyter_env python=3.10 -y

# Activate the environment
conda activate jupyter_env
```

---

## 3. Install Jupyter Notebook

```bash
# Install Jupyter Notebook
conda install jupyter -y
```

Or you can use `pip` inside the environment:

```bash
pip install notebook
```

---

## 4. Run Jupyter Notebook

Once installed, start the notebook server:

```bash
jupyter notebook
```

- This will open a **web browser** at:  
  [http://localhost:8888](http://localhost:8888)

- You can now create new notebooks (`.ipynb`) and start coding in Python.

---

## 5. (Optional) Install JupyterLab

JupyterLab is a modern interface for Jupyter Notebooks.

```bash
conda install jupyterlab -y
# or
pip install jupyterlab
```

Run it with:

```bash
jupyter lab
```

---

## Summary

1. Install Miniforge.  
2. Create and activate a Python environment.  
3. Install Jupyter Notebook.  
4. Run with `jupyter notebook`.  

You are now ready to use Jupyter for data science and Python projects! 🚀
