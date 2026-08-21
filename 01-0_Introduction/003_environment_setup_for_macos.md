# Environment Setup for macOS

Use this guide for macOS 14 or later. Start at Step 1 and complete one step at a time. You do not need to understand every command yet.

## 1. Install Command-Line Tools and Homebrew

Open Terminal and run:

```bash
xcode-select --install
```

After the installer finishes, run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Follow the final Homebrew message, then open a new Terminal window. Homebrew helps macOS install programming tools.

## 2. Install Python, Git, and VS Code

```bash
brew install python@3.12 git
brew install --cask visual-studio-code
python3.12 --version
```

The last command should show `Python 3.12`.

## 3. Download the Course Repository

```bash
cd ~
git clone https://github.com/sonamu-jun/introduction-to-bigdata.git
cd introduction-to-bigdata
```

For later updates, use the GitHub guide: [Download and update the course files](004_github_download_and_update.md).

## 4. Create the Course Environment

This creates a separate Python workspace for this course. Run these commands inside the `introduction-to-bigdata` folder.

```bash
python3.12 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## 5. Open VS Code and Run a Notebook

Open VS Code, choose `File` then `Open Folder`, and select `introduction-to-bigdata`.

In the Extensions view, install:

- Python
- Jupyter
- Pylance

Then:

1. Press `Command+Shift+P`.
2. Choose `Python: Select Interpreter`.
3. Select the interpreter ending in `.venv/bin/python`.
4. Open a course notebook and select `Select Kernel`.
5. Select the same `.venv` environment.
6. Run the first code cell.

If you cannot find `.venv/bin/python`, ask your instructor for help.
