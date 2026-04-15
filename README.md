# 🐼 Pandas Project

A Python project using [pandas](https://pandas.pydata.org/) for data analysis and manipulation.

---

## 📋 Requirements

- Python 3.8 or higher
- pip (comes bundled with Python)

---

## 🪟 Setup — Windows Virtual Environment

Follow these steps to create and activate a Python virtual environment on **Windows**.

### 1. Clone or Download the Project

```bash
git clone https://github.com/JaneCS2025/crm.git
cd crm
```

### 2. Create a Virtual Environment

Open **Command Prompt** or **PowerShell** and run:

```bash
python -m venv venv
```

This creates a `venv` folder in your project directory.

### 3. Activate the Virtual Environment

**Command Prompt:**

```bash
venv\Scripts\activate.bat
```

**PowerShell:**

```powershell
venv\Scripts\Activate.ps1
```

> ⚠️ If you get a PowerShell execution policy error, run this first:
>
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

Once activated, your terminal prompt will show `(venv)`.

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Verify Installation

```bash
python -c "import pandas; print(pandas.__version__)"
```

---

## 🧪 JupyterLab — Install & Run in Virtual Environment

### 1. Activate Your Virtual Environment First

**Command Prompt:**

```bash
venv\Scripts\activate.bat
```

**PowerShell:**

```powershell
venv\Scripts\Activate.ps1
```

### 2. Install JupyterLab

```bash
pip install jupyterlab
```

### 3. Launch JupyterLab

```bash
jupyter lab
```

This will open JupyterLab in your default browser at `http://localhost:8888`.

### 4. Install the Virtual Environment as a Jupyter Kernel (Recommended)

So JupyterLab uses your venv's Python and packages:

```bash
pip install ipykernel
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```

Then in JupyterLab, select **"Python (venv)"** as the kernel when creating a new notebook.

### 5. Stop JupyterLab

Press `Ctrl + C` in the terminal to shut down the JupyterLab server.

---

## 🚀 Usage

```python
import pandas as pd

# Example: Create a DataFrame
df = pd.DataFrame({
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35]
})

print(df)
```

---

## 🛑 Deactivate the Virtual Environment

When you're done, deactivate the environment by running:

```bash
deactivate
```

---

## 📁 Project Structure

```
pandas/
├── venv/               # Virtual environment (not committed to git)
├── requirements.txt     # Project dependencies
└── README.md            # Project documentation
```

---

## 📝 Notes

- Never commit the `venv` folder to Git. Make sure `venv` is listed in your `.gitignore`.
- To regenerate `requirements.txt` after installing new packages:
  ```bash
  pip freeze > requirements.txt
  ```
