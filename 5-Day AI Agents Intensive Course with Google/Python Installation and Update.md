
# 🐍 **Check and Update Python (Windows + macOS)**

---

## 🔍 1️⃣ Check your current Python version

### 💻 Command (same for both systems)

```bash
python --version
```

or

```bash
python3 --version
```

📝 **Output example:**

```
Python 3.9.6
```

> ✅ You’ll want **Python 3.10 or higher** (e.g., 3.11 or 3.12).

---

## ⚙️ 2️⃣ Update Python (choose your system)

---

### 🪟 **For Windows**

#### 🧩 Step 1: Download

Go to 👉 [https://www.python.org/downloads/](https://www.python.org/downloads/)  
Click **“Download Python 3.x.x”** (latest stable version).

#### 🧰 Step 2: Install

1. Run the installer.
    
2. ✅ **Check the box** “Add Python to PATH”.
    
3. Click **Customize installation → Next → Install**.
    
4. Wait till it finishes.
    

#### 🧾 Step 3: Verify

Open Command Prompt and run:

```bash
python --version
```

or

```bash
py --version
```

You should now see the new version (e.g., `Python 3.12.2`).

---

### 🍎 **For macOS**

#### 🧩 Option 1: Using Homebrew (recommended)

If you have Homebrew installed, run:

```bash
brew update
brew install python
```

If you already had Python, upgrade it:

```bash
brew upgrade python
```

Then verify:

```bash
python3 --version
```

#### 🧩 Option 2: Manual Install

If you don’t have Homebrew, go to:  
👉 [https://www.python.org/downloads/macos/](https://www.python.org/downloads/macos/)  
Download and install the latest `.pkg` file.

After installation:

```bash
python3 --version
```

---

## 🧹 3️⃣ (Optional) Set your default Python to new version

If multiple versions exist, make sure `python` points to the new one.

### 💻 For both macOS & Linux:

```bash
which python3
```

To update symlink (⚠️ advanced):

```bash
sudo ln -sf $(which python3) /usr/local/bin/python
```

### 🪟 For Windows:

Run:

```bash
py -0
```

Then set default with:

```bash
py -3.12
```

---

## ✅ 4️⃣ Upgrade pip (after updating Python)

```bash
python3 -m pip install --upgrade pip
```

---

## 🧠 Quick Summary

|Task|Command (Windows)|Command (macOS)|
|---|---|---|
|Check version|`python --version`|`python3 --version`|
|Install/upgrade|Installer (python.org)|`brew upgrade python`|
|Verify update|`py --version`|`python3 --version`|
|Update pip|`python -m pip install --upgrade pip`|`python3 -m pip install --upgrade pip`|

---

Would you like me to write this as a **Markdown tutorial note** (like for your Obsidian vault)?  
I can format it cleanly with emojis, numbered sections, and examples for beginners.