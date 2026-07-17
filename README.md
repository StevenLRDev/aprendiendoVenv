# Basic Python Environment Configuration

## Overview

A **Virtual Environment (VE)** is an isolated environment where Python dependencies are installed for a specific project.

### Why use a Virtual Environment?

- Prevents conflicts between projects.
- Keeps project dependencies isolated.
- Avoids installing every library globally on your computer.
- Makes projects easier to share and maintain.

---

# Step 1 - Create a Virtual Environment

Execute the following command in your project directory:

```bash
python -m venv venv
```

### What happens?

A new folder named `venv` will be created containing all the files required for the virtual environment.

Example:

```
Project/
│
├── venv/
├── main.py
└── requirements.txt
```

---

# Step 2 - Navigate to the Scripts Folder

Move into the virtual environment directories:

```bash
cd venv
cd Scripts
```

---

# Step 3 - Activate the Virtual Environment

Run:

```bash
activate
```

If activated successfully, your terminal prompt should change from:

```text
C:\Project>
```

to:

```text
(venv) C:\Project>
```

The `(venv)` prefix indicates that the virtual environment is active.

---

# Step 4 - Return to the Project Root

After activation, navigate back to the project folder.

```bash
cd ..
```

Output:

```text
(venv) C:\Project\venv
```

Again:

```bash
cd ..
```

Output:

```text
(venv) C:\Project
```

Now you're ready to install packages.

---

# Step 5 - Install Required Libraries

Install **Pandas**

```bash
pip install pandas
```

Install **Matplotlib**

```bash
pip install matplotlib
```

Install **Requests**

```bash
pip install requests
```

Once installed, the packages become available only inside the active virtual environment.

---

# Step 6 - Verify Installed Packages

Display every installed package:

```bash
pip freeze
```

Example output:

```text
matplotlib==3.x.x
numpy==2.x.x
pandas==2.x.x
requests==2.x.x
```

This command shows the list of libraries currently installed in the virtual environment.

---

# Useful Commands

| Command | Description |
|----------|-------------|
| `python -m venv venv` | Create a virtual environment |
| `cd venv` | Enter the virtual environment folder |
| `cd Scripts` | Open the Scripts directory |
| `activate` | Activate the virtual environment |
| `cd ..` | Return to the previous directory |
| `pip install pandas` | Install Pandas |
| `pip install matplotlib` | Install Matplotlib |
| `pip install requests` | Install Requests |
| `pip freeze` | Display all installed packages |

---

# Workflow Summary

```text
Create Project
      │
      ▼
python -m venv venv
      │
      ▼
cd venv
      │
      ▼
cd Scripts
      │
      ▼
activate
      │
      ▼
(venv) C:\Project>
      │
      ▼
cd ..
cd ..
      │
      ▼
pip install pandas
pip install matplotlib
pip install requests
      │
      ▼
pip freeze
```

---

# Notes

- Always activate the virtual environment before installing packages.
- Packages installed inside a virtual environment do not affect other Python projects.
- Use `pip freeze` to review all installed dependencies.
- The `(venv)` prefix in the terminal confirms that the virtual environment is currently active.
