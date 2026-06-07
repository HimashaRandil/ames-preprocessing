# 🏠 Ames Housing — Pre-Modeling Data Preprocessing

A practical, lecture-ready Jupyter notebook covering end-to-end data preprocessing for regression tasks — including missing value treatment, outlier detection, encoding strategies, feature scaling, and sklearn pipeline construction.

---

## 📋 Table of Contents

- [What You Need Before Starting](#what-you-need-before-starting)
- [Step 1 — Install Python](#step-1--install-python)
- [Step 2 — Install VS Code](#step-2--install-vs-code)
- [Step 3 — Install VS Code Extensions](#step-3--install-vs-code-extensions)
- [Step 4 — Install uv](#step-4--install-uv)
- [Step 5 — Clone the Repository](#step-5--clone-the-repository)
- [Step 6 — Download the Dataset](#step-6--download-the-dataset)
- [Step 7 — Set Up the Virtual Environment](#step-7--set-up-the-virtual-environment)
- [Step 8 — Open the Notebook in VS Code](#step-8--open-the-notebook-in-vs-code)
- [Folder Structure](#folder-structure)
- [Troubleshooting](#troubleshooting)

---

## What You Need Before Starting

You will need to install the following tools. Each one is covered step by step below.

| Tool | Purpose |
|------|---------|
| **Python 3.10+** | The programming language we use |
| **VS Code** | The code editor we use |
| **uv** | A fast Python package manager |
| **Git** | To clone the project from GitHub |

---

## Step 1 — Install Python

### Windows

1. Open your browser and go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click the yellow **Download Python 3.x.x** button (the latest version is fine)
3. Once downloaded, open the installer
4. ⚠️ **Important:** At the bottom of the first screen, check the box that says **"Add Python to PATH"** — this is critical
5. Click **Install Now**
6. Wait for the installation to complete, then click **Close**

**Verify installation:**
1. Press `Windows + R`, type `cmd`, press Enter
2. In the black window that opens, type:
   ```
   python --version
   ```
3. You should see something like `Python 3.12.3` — if you do, Python is installed correctly

### Mac

1. Open your browser and go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click the yellow **Download Python 3.x.x** button
3. Once downloaded, open the `.pkg` file
4. Follow the installation steps — click Continue, Agree, and Install
5. Enter your Mac password if prompted

**Verify installation:**
1. Press `Command + Space`, type `Terminal`, press Enter
2. In the Terminal window, type:
   ```
   python3 --version
   ```
3. You should see something like `Python 3.12.3`

---

## Step 2 — Install VS Code

Visual Studio Code (VS Code) is the code editor we will use to run the notebook.

### Windows

1. Go to [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Click the blue **Download for Windows** button
3. Open the downloaded `.exe` file
4. Accept the license agreement and click **Next**
5. On the "Select Additional Tasks" screen, check all of the following:
   - ✅ Add "Open with Code" action to Windows Explorer file context menu
   - ✅ Add "Open with Code" action to Windows Explorer directory context menu
   - ✅ Add to PATH
6. Click **Next**, then **Install**
7. Once done, click **Finish** — VS Code will open automatically

### Mac

1. Go to [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Click the blue **Download for Mac** button
3. Once downloaded, open the `.zip` file — it will extract a file called `Visual Studio Code`
4. **Drag** the `Visual Studio Code` application into your **Applications** folder
5. Open it from your Applications folder
6. If you see a warning saying "Apple cannot verify this app", click **Open Anyway**

**Add VS Code to your terminal (Mac only):**
1. Open VS Code
2. Press `Command + Shift + P` to open the command palette
3. Type `shell command` and click **Shell Command: Install 'code' command in PATH**
4. Close and reopen your Terminal

---

## Step 3 — Install VS Code Extensions

Extensions add extra features to VS Code. We need two.

1. Open VS Code
2. On the left sidebar, click the **Extensions** icon (it looks like four squares)
3. In the search box, search for and install each of the following:

**Extension 1 — Python:**
- Search: `Python`
- Publisher: Microsoft
- Click **Install**

**Extension 2 — Jupyter:**
- Search: `Jupyter`
- Publisher: Microsoft
- Click **Install**

Once both are installed, close and reopen VS Code.

---

## Step 4 — Install uv

`uv` is a fast Python package manager. It reads the `pyproject.toml` file in this project and installs all required libraries automatically.

### Windows

1. Press `Windows + R`, type `cmd`, press Enter
2. In the command prompt, paste this command and press Enter:
   ```
   powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
   ```
3. Wait for it to finish — you will see a success message
4. **Close and reopen** the command prompt window

**Verify installation:**
```
uv --version
```
You should see something like `uv 0.4.x`

### Mac

1. Open Terminal (`Command + Space`, type Terminal, press Enter)
2. Paste this command and press Enter:
   ```
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```
3. Wait for it to finish
4. **Close and reopen** the Terminal window

**Verify installation:**
```
uv --version
```
You should see something like `uv 0.4.x`

---

## Step 5 — Clone the Repository

### If you do not have Git installed

**Windows:**
1. Go to [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Download and run the installer — click Next through all steps with default settings

**Mac:**
1. Open Terminal and type:
   ```
   git --version
   ```
2. If Git is not installed, Mac will automatically prompt you to install it — click **Install**

### Clone the project

**Windows:**
1. Open File Explorer and navigate to the folder where you want to save the project (e.g. your Desktop or Documents)
2. Right-click in an empty area and select **Open in Terminal** (or **Open Git Bash here**)
3. Type the following command and press Enter:
   ```
   git clone https://github.com/HimashaRandil/ames-preprocessing.git
   ```
4. A folder called `ames-preprocessing` will appear

**Mac:**
1. Open Terminal
2. Navigate to where you want to save the project. For example, to save it on your Desktop:
   ```
   cd ~/Desktop
   ```
3. Then clone the repo:
   ```
   git clone https://github.com/YOUR-USERNAME/ames-preprocessing.git
   ```
4. A folder called `ames-preprocessing` will appear on your Desktop

---

## Step 6 — Download the Dataset

1. Go to [https://www.kaggle.com/datasets/prevek18/ames-housing-dataset](https://www.kaggle.com/datasets/prevek18/ames-housing-dataset)
2. You will need a free Kaggle account — sign up if you do not have one
3. Click the **Download** button
4. Extract the downloaded `.zip` file
5. Find the file called `AmesHousing.csv`
6. Copy or move it into the `data/` folder inside the `ames-preprocessing` project folder

Your folder should now look like this:
```
ames-preprocessing/
└── data/
    └── AmesHousing.csv   ← file goes here
```

---

## Step 7 — Set Up the Virtual Environment

A virtual environment is an isolated space where we install the project's libraries without affecting anything else on your computer.

### Windows

1. Open the `ames-preprocessing` folder in File Explorer
2. Right-click in an empty area inside the folder and select **Open in Terminal**
3. Run the following commands one by one, pressing Enter after each:

```
uv sync
```

This will:
- Read the `pyproject.toml` file
- Create a `.venv` folder inside the project
- Install all required libraries automatically

4. Once done, activate the environment:
```
.venv\Scripts\activate
```

You will see `(ames-preprocessing)` appear at the start of your terminal line — this means the environment is active.

5. Register the environment as a Jupyter kernel:
```
python -m ipykernel install --user --name=ames-preprocess --display-name "Ames Preprocessing"
```

### Mac

1. Open Terminal
2. Navigate into the project folder:
   ```
   cd ~/Desktop/ames-preprocessing
   ```
   (adjust the path if you saved it somewhere else)

3. Run:
   ```
   uv sync
   ```

4. Activate the environment:
   ```
   source .venv/bin/activate
   ```

   You will see `(ames-preprocessing)` appear at the start of your terminal line.

5. Register the environment as a Jupyter kernel:
   ```
   python -m ipykernel install --user --name=ames-preprocess --display-name "Ames Preprocessing"
   ```

---

## Step 8 — Open the Notebook in VS Code

### Windows

1. Open the `ames-preprocessing` folder in File Explorer
2. Right-click inside the folder and select **Open with Code**
3. VS Code will open with the full project visible in the left sidebar

### Mac

1. Open Terminal and navigate to the project folder:
   ```
   cd ~/Desktop/ames-preprocessing
   ```
2. Type:
   ```
   code .
   ```
3. VS Code will open with the full project visible in the left sidebar

### Select the correct kernel

1. In the left sidebar, click on `notebooks/` and open `ames_preprocessing.ipynb`
2. In the top right corner of the notebook, you will see a button that says **Select Kernel**
3. Click it
4. A dropdown will appear — select **Ames Preprocessing**
   - It will appear as `cpython-3.10.x` with the label `Virtual Env`
5. You are now ready to run the notebook

### Run the notebook

- To run a single cell: click on it and press `Shift + Enter`
- To run all cells from the top: click **Run All** in the top toolbar
- Always run cells from top to bottom — do not skip cells

---

## Folder Structure

```
ames-preprocessing/
│
├── data/
│   └── AmesHousing.csv          ← dataset (you add this manually)
│
├── notebooks/
│   └── ames_preprocessing.ipynb ← main notebook
│
├── assets/
│   ├── skewness.png             ← diagram used in notebook
│   └── log_transformation.png  ← diagram used in notebook
│
├── outputs/
│   └── (plots saved here when you run the notebook)
│
├── src/
│   └── (empty — for future helper functions)
│
├── pyproject.toml               ← project dependencies
├── .venv/                       ← virtual environment (auto-created by uv)
└── README.md                    ← this file
```

---

## Troubleshooting

**`uv` command not found after installation**
- Close your terminal completely and open a new one
- The PATH update only takes effect in a new terminal window

**Kernel not showing up in VS Code**
- Make sure you ran the `ipykernel install` command in Step 7
- Restart VS Code completely and try again
- Click the refresh icon in the kernel picker dropdown

**`ModuleNotFoundError` when running a cell**
- Make sure the `(ames-preprocessing)` environment is active in your terminal
- Make sure you selected the **Ames Preprocessing** kernel in VS Code
- Run `uv sync` again in the project folder to ensure all packages are installed

**`AmesHousing.csv` not found error**
- Check that the file is inside the `data/` folder — not inside a subfolder within `data/`
- Check that the filename is exactly `AmesHousing.csv` — spelling and capitalisation matter

**Permission error on Mac when running `uv` install**
- Try running the command with `sudo`:
  ```
  sudo curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

**VS Code shows "Select Kernel" but Ames Preprocessing is not listed**
- Go back to your terminal, make sure the environment is activated, and re-run:
  ```
  python -m ipykernel install --user --name=ames-preprocess --display-name "Ames Preprocessing"
  ```
- Then reload VS Code with `Command + Shift + P` → **Developer: Reload Window**

---

## Libraries Used

| Library | Version | Purpose |
|---------|---------|---------|
| `pandas` | ≥2.0 | Data manipulation |
| `numpy` | ≥1.24 | Numerical computing |
| `matplotlib` | ≥3.7 | Plotting |
| `seaborn` | ≥0.12 | Statistical visualisation |
| `scikit-learn` | ≥1.3 | Preprocessing and modeling |
| `ydata-profiling` | ≥4.6 | Automated EDA report |
| `missingno` | ≥0.5 | Missing value visualisation |
| `scipy` | ≥1.11 | Statistical testing |
| `jupyter` | ≥1.0 | Notebook interface |
| `ipykernel` | ≥6.0 | Jupyter kernel support |
