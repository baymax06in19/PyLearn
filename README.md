```____       __                      
   / __ \__  _/ /   ___  ____ _________ 
  / /_/ / / / / /   / _ \/ __ `/ ___/ __ \
 / ____/ /_/ / /___/  __/ /_/ / /  / / / /
/_/    \__, /_____/\___/\__,_/_/  /_/ /_/ 
      /____/                    🐍
```
# Python — Introduction

## What is Python?

Python is a **high-level, interpreted programming language** known for simplicity and readability.

**Created by:** Guido van Rossum  
**First Released:** 1991  
**Name Origin:** Inspired by "Monty Python's Flying Circus"

---

### Key Characteristics

| Feature | Description |
|---------|-------------|
| **High-Level** | Abstract away hardware details |
| **Interpreted** | No compilation needed — run immediately |
| **Readable** | Clean syntax, fewer lines of code |
| **Multi-Paradigm** | Supports procedural, OOP, functional programming |

---

### Why Python?

**Simplicity**  
Code reads almost like English — easy to learn and maintain.

**Extensive Libraries**  
Vast ecosystem for any task:
- Data Science: NumPy, Pandas, Matplotlib
- Machine Learning: TensorFlow, PyTorch, Scikit-learn
- Web Development: Django, Flask
- Automation: Selenium, Requests

**Versatility**  
Used across domains: AI, web, automation, research, education.

**Strong Community**  
Active support, extensive documentation, welcoming to beginners.

---

## Python 2 vs Python 3

Python 3 was created to fix design flaws in Python 2.

### Key Differences

| Feature | Python 2 | Python 3 |
|---------|----------|----------|
| **Print** | `print "Hello"` | `print("Hello")` |
| **Division** | `5 / 2 = 2` | `5 / 2 = 2.5` |
| **Unicode** | ASCII default | Unicode default |
| **Range** | Returns list | Returns iterator |
| **Strings** | `str` (bytes) | `str` (text) |

---

### Examples

**Print Statement**
```python
# Python 2
print "Hello, World!"

# Python 3
print("Hello, World!")
```

**Division**
```python
# Python 2
5 / 2      # Output: 2 (integer)

# Python 3
5 / 2      # Output: 2.5 (float)
5 // 2     # Output: 2 (integer)
```

---

## Timeline

| Year | Event |
|------|-------|
| 1991 | Python 0.9.0 released |
| 2000 | Python 2.0 released |
| 2008 | Python 3.0 released |
| 2020 | Python 2 reached EOL (End of Life) |

**Current Status:**  
Python 2 is dead. Always use **Python 3** for new projects.

---

## Where Python is Used

### ✅ Popular Applications

- **Data Science & AI** — #1 choice for ML/AI
- **Web Development** — Backend APIs, web apps
- **Automation** — Task automation, scripting
- **Scientific Research** — Physics, biology, chemistry
- **Education** — Teaching programming

### Core Concepts

Like any programming language, Python has fundamental building blocks:

| Concept | Purpose | Example |
|---------|---------|---------|
| **Variables** | Store data | `age = 25` |
| **Conditions** | Make decisions | `if age > 18:` |
| **Loops** | Repeat operations | `for i in range(10):` |
| **Functions** | Reusable code | `def calculate():` |
| **Data Structures** | Organize data | Lists, dictionaries |
...

These core elements can express **any logic** — from simple scripts to complex AI systems.

---

## How to Use Python in our learning?

Two main approaches:

### 1. Write in .py files
You can install Python on your machine and write programs in `.py` files.
<a href="https://www.python.org/downloads/">install Python</a>

### 2. Use jupyter notebook
You can use Jupyter for interactive coding and experimentation.
<a href="https://jupyterlab.readthedocs.io/en/latest/getting_started/installation.html#">install Jupyter labs</a>

---

## Summary

- Python is **simple, readable, and powerful**
- Python 3 is the **modern standard** (Python 2 is obsolete)
- **Extensive libraries** for any domain
- Core concepts: **variables, conditions, loops, functions**
- Ideal for: **AI , Data science, web, automation, learning**

---
```
███████╗███╗   ██╗██████╗ 
██╔════╝████╗  ██║██╔══██╗
█████╗  ██╔██╗ ██║██║  ██║  
██╔══╝  ██║╚██╗██║██║  ██║
███████╗██║ ╚████║██████╔╝
╚══════╝╚═╝  ╚═══╝╚═════╝
```








## Additional deatils refer:

### Understanding PATH and Python

### What is PATH?

**PATH** is an **environment variable** in your operating system that tells the system **where to look for executable programs**.

Think of it like a **contact list** on your phone — when you want to call someone, you don't memorize their number. You just search by name, and your phone finds the number from your contact list.

Similarly, when you type a command like `python` in your terminal, your operating system searches through the PATH to find where the `python` executable is located.

---

### How PATH Works

#### Without Understanding PATH

When you type a command in your terminal:

```bash
python script.py
```

Your operating system needs to answer: **"Where is python?"**

---

#### The Search Process

```
You type: python script.py
         ↓
OS asks: "Where is the 'python' program?"
         ↓
OS checks PATH variable
         ↓
PATH contains multiple directories:
  → /usr/local/bin
  → /usr/bin
  → /bin
  → /home/user/.local/bin
         ↓
OS searches each directory in order
         ↓
Found python in: /usr/local/bin/python
         ↓
Executes: /usr/local/bin/python script.py
```

---

### What is an Environment Variable?

Environment variables are **named values** stored by the operating system that programs can access.

#### Common Environment Variables

| Variable | Purpose | Example Value |
|----------|---------|---------------|
| **PATH** | Directories to search for executables | `/usr/bin:/usr/local/bin` |
| **HOME** | User's home directory | `/home/username` |
| **USER** | Current username | `alice` |
| **PYTHONPATH** | Where Python looks for modules | `/usr/lib/python3.9` |

---

### Viewing Your PATH

#### On Windows (Command Prompt)
```cmd
echo %PATH%
```

#### On Windows (PowerShell)
```powershell
$env:PATH
```

#### On macOS/Linux
```bash
echo $PATH
```

#### Example Output
```
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/home/user/.local/bin
```

Each directory is separated by:
- `:` (colon) on macOS/Linux
- `;` (semicolon) on Windows

---

### Why Do We Need to Add Python to PATH?

#### Problem Without Python in PATH

Let's say Python is installed at: `/Users/alice/Python3.11/python`

**Scenario 1: Python NOT in PATH**

```bash
# You type:
python script.py

# Result:
bash: python: command not found
```

**Why?** The OS doesn't know where to find `python`.

---

**Solution Without PATH (Manual)**

You'd have to type the **full path** every time:

```bash
/Users/alice/Python3.11/python script.py
```

This is:
- ❌ Tedious
- ❌ Error-prone
- ❌ Not portable (different on every machine)

---

**Scenario 2: Python IS in PATH**

```bash
# You type:
python script.py

# Result:
✓ Script runs successfully!
```

**Why?** The OS finds `python` automatically by searching PATH.

---

### How to Add Python to PATH

#### Windows

##### Method 1: During Installation (Recommended)
When installing Python, check the box:
```
☑ Add Python 3.x to PATH
```

<img src="images/python-install-path.png" width="400" alt="Python installer PATH option">

##### Method 2: Manually (After Installation)

1. **Find Python installation directory**
   - Usually: `C:\Users\YourName\AppData\Local\Programs\Python\Python311`

2. **Open System Environment Variables**
   - Search "Environment Variables" in Start Menu
   - Click "Edit the system environment variables"
   - Click "Environment Variables" button

3. **Edit PATH**
   - Under "User variables" or "System variables"
   - Select "Path"
   - Click "Edit"
   - Click "New"
   - Add: `C:\Users\YourName\AppData\Local\Programs\Python\Python311`
   - Add: `C:\Users\YourName\AppData\Local\Programs\Python\Python311\Scripts`

4. **Apply and Restart**
   - Click OK on all dialogs
   - Restart Command Prompt/PowerShell

---

#### macOS/Linux

##### Method 1: Check Current PATH
```bash
echo $PATH
```

##### Method 2: Add to Shell Configuration

**For Bash (older macOS, most Linux)**

Edit `~/.bashrc` or `~/.bash_profile`:
```bash
export PATH="/usr/local/bin/python3:$PATH"
```

**For Zsh (newer macOS default)**

Edit `~/.zshrc`:
```bash
export PATH="/usr/local/bin/python3:$PATH"
```

##### Method 3: Apply Changes
```bash
source ~/.zshrc    # For Zsh
# or
source ~/.bashrc   # For Bash
```

---

### Verifying Python is in PATH

After adding Python to PATH, verify it works:

```bash
# Check if python command works
python --version
# or
python3 --version

# Check where python is located
which python      # macOS/Linux
where python      # Windows
```

#### Expected Output
```
Python 3.11.5
```

If you see this, ✅ Python is successfully in PATH!

---

### What Happens Behind the Scenes?

#### Example: Running `python script.py`

```
Step 1: You type "python script.py"
         ↓
Step 2: Shell looks for "python" executable
         ↓
Step 3: Shell reads PATH variable
        PATH = "/usr/local/bin:/usr/bin:/bin"
         ↓
Step 4: Searches each directory in order:
        - Check /usr/local/bin/python → Not found
        - Check /usr/bin/python → Found! ✓
         ↓
Step 5: Execute /usr/bin/python with argument "script.py"
         ↓
Step 6: Python interpreter runs your script
```

---

### Common PATH Issues

#### Issue 1: "python: command not found"

**Cause:** Python not in PATH

**Solution:**
- Add Python installation directory to PATH
- Or use full path: `/usr/local/bin/python3 script.py`

---

#### Issue 2: Wrong Python Version Running

**Cause:** Multiple Python versions installed, wrong one found first in PATH

**Example:**
```bash
# PATH = "/usr/bin:/usr/local/bin"
# Both contain python

/usr/bin/python       → Python 2.7
/usr/local/bin/python → Python 3.11

# Typing "python" runs Python 2.7 (found first)
```

**Solution:**
- Reorder PATH to prioritize desired version
- Use specific command: `python3` instead of `python`

---

#### Issue 3: PATH Not Persisting After Reboot

**Cause:** PATH modified only for current session

**Solution:**
- Edit shell configuration file (`~/.bashrc`, `~/.zshrc`)
- Use system environment variables (Windows)

---

### Why Multiple Directories in PATH?

Different directories serve different purposes:

| Directory | Purpose | Example Programs |
|-----------|---------|------------------|
| `/usr/bin` | System programs | `ls`, `cat`, `grep` |
| `/usr/local/bin` | User-installed programs | Custom Python, Node.js |
| `/bin` | Essential system binaries | `bash`, `sh` |
| `~/.local/bin` | User-specific programs | `pip` installed tools |

Having multiple directories lets you:
- Keep system and user programs separate
- Install programs without admin rights (in user directories)
- Override system programs with custom versions

---

### PATH and Other Programming Languages

PATH isn't just for Python — it's used for **all** command-line programs:

| Language/Tool | Executable | Why in PATH |
|---------------|-----------|-------------|
| **Python** | `python`, `pip` | Run scripts, install packages |
| **Node.js** | `node`, `npm` | Run JS programs, install packages |
| **Java** | `java`, `javac` | Compile and run Java programs |
| **Git** | `git` | Version control commands |
| **Ruby** | `ruby`, `gem` | Run scripts, install gems |

---

### Best Practices

#### ✅ Do's

1. **Add to PATH during installation**
   - Check the "Add to PATH" box during install

2. **Use virtual environments**
   - Don't pollute global PATH
   - Use `venv` or `conda` environments

3. **Keep PATH organized**
   - Remove unused entries
   - Prioritize important directories first

4. **Use specific commands**
   - Use `python3` instead of `python` for clarity
   - Use `pip3` instead of `pip`

---

#### ❌ Don'ts

1. **Don't add too many directories**
   - Slows down command lookup
   - Creates confusion

2. **Don't override system programs**
   - Be careful when adding directories to the start of PATH

3. **Don't modify PATH manually every time**
   - Use configuration files for persistence

---

### Real-World Analogy

Think of your operating system as a **library** and executables as **books**.

**Without PATH:**
- You know a book called "Python" exists
- But you don't know which shelf it's on
- You'd have to memorize: "3rd floor, section B, shelf 7"

**With PATH:**
- PATH is like a "frequently used" bookmark list
- You tell the librarian: "Find Python"
- Librarian checks the bookmark list (PATH)
- Finds it and retrieves it for you

---

### Advanced: PYTHONPATH vs PATH

#### PATH
- Tells OS **where to find executables**
- Example: Where is the `python` program?

#### PYTHONPATH
- Tells Python **where to find modules**
- Example: Where is the `numpy` library?

```bash
# PATH - Finding the python executable
PATH=/usr/local/bin:/usr/bin

# PYTHONPATH - Finding Python modules
PYTHONPATH=/home/user/my_modules:/usr/lib/python3.9
```

---

### Summary

| Concept | Explanation |
|---------|-------------|
| **PATH** | List of directories where OS searches for programs |
| **Why needed?** | So you can type `python` instead of full path |
| **Environment Variable** | Named value stored by OS |
| **How to add?** | During install or edit system settings |
| **Verification** | `python --version` should work |
| **Common issue** | "command not found" = not in PATH |

---

### Quick Reference Commands

```bash
# View PATH
echo $PATH                    # macOS/Linux
echo %PATH%                   # Windows CMD
$env:PATH                     # Windows PowerShell

# Check Python location
which python                  # macOS/Linux
where python                  # Windows

# Add to PATH (current session only)
export PATH="/new/path:$PATH" # macOS/Linux
$env:PATH += ";C:\new\path"   # Windows PowerShell

# Verify Python works
python --version
python3 --version
pip --version
```

---
