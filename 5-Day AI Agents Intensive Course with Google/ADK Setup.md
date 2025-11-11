# 🧠 Google Agent Development Kit (ADK) — Python Quickstart Tutorial

This tutorial walks you step-by-step through setting up and running an AI **Agent** using **Google’s ADK (Agent Development Kit)** in **Python**.
By the end, you’ll have your own agent running both in the **terminal** and via a **web interface**.

---

## 🪴 1. Prerequisites

Before starting, make sure you have:

* 🐍 **Python 3.10 or later**    [[Python Installation and Update]]
* 💾 **pip** (Python package manager)
* 🌐 Internet access
* 🧰 A **Google API key** (get it from [Google AI Studio → API Keys](https://aistudio.google.com/apikey))

---

## 🧱 2. Set Up Your Project

### Step 1️⃣ — Create a project folder

Open your terminal and run:

```bash
mkdir -p ~/projects
cd ~/projects
```

### Step 2️⃣ — Create a virtual environment

This isolates your dependencies.

```bash
python3 -m venv .venv
source .venv/bin/activate
```

💡 You’ll now see `(.venv)` at the start of your terminal prompt — this means the virtual environment is active.

---

## ⚙️ 3. Install the ADK

Install the Agent Development Kit using pip:

```bash
pip install google-adk
```

---

## 🤖 4. Create Your Agent

Run the ADK command to create a new agent project:

```bash
adk create my_agent
```

You’ll be guided through a short setup:

```
Choose a model for the root agent:
1. gemini-2.5-flash
2. Other models (fill later)
Choose model (1, 2): 1

3. Google AI
4. Vertex AI
Choose a backend (1, 2): 1
```

Then enter your **Google API key** (you can generate one from AI Studio):

```
Enter Google API key: [paste your key here]
```

✅ Once done, ADK creates your project with this structure:

```
my_agent/
 ├── agent.py      # main agent logic
 ├── .env          # stores API keys
 └── __init__.py
```

---

## 🧩 5. Run Your Agent in the Terminal

Go inside the agent folder:

```bash
cd my_agent
```

Then run the agent:

```bash
adk run
```

You’ll now enter an interactive session:

```
Running agent root_agent, type exit to exit.
[user]: What's the time in Tokyo?

[root_agent]: The current time in Tokyo is Monday, July 29, 2024, 11:24 PM (JST).
```

🎉 Your agent is working!

To stop, type:

```
exit
```

---

## 💻 6. Run the Agent in a Web Interface

Go back to the parent folder:

```bash
cd ..
```

Then launch the ADK web UI:

```bash
adk web --port 8000
```

If everything is set up correctly, you’ll see:

```
+-----------------------------------------------------------------------------+
| ADK Web Server started                                                      |
|                                                                             |
| For local testing, access at http://127.0.0.1:8000                          |
+-----------------------------------------------------------------------------+
```

🌐 Open [http://localhost:8000](http://localhost:8000) in your browser —
you’ll get a **chat interface** to interact with your agent visually!

---

## 🧹 7. Close or Deactivate the Virtual Environment

When you’re done:

```bash
deactivate
```

This returns you to your system’s default Python environment.

---

## ⚡ Common Issues

| Error                                   | Cause                  | Solution                           |
| --------------------------------------- | ---------------------- | ---------------------------------- |
| `MCP requires Python 3.10 or above`     | Python version too old | Upgrade to Python 3.10+            |
| `Form data requires "python-multipart"` | Missing dependency     | Run `pip install python-multipart` |
| `NotOpenSSLWarning`                     | macOS uses LibreSSL    | Safe to ignore for most users      |

---

## ✅ Summary

| Step | Action                | Command                                              |
| ---- | --------------------- | ---------------------------------------------------- |
| 1    | Create project folder | `mkdir -p ~/projects && cd ~/projects`               |
| 2    | Create venv           | `python3 -m venv .venv && source .venv/bin/activate` |
| 3    | Install ADK           | `pip install google-adk`                             |
| 4    | Create agent          | `adk create my_agent`                                |
| 5    | Run agent             | `cd my_agent && adk run`                             |
| 6    | Web interface         | `cd .. && adk web --port 8000`                       |
| 7    | Exit venv             | `deactivate`                                         |

---
