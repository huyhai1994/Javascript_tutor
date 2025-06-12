Sure! Here's a complete, beginner-friendly guide to **install, manage, and use `nvm` (Node Version Manager) and Node.js on Windows**.

---

## ✅ 1. Install `nvm` for Windows

> The official Linux/Mac nvm doesn't work on Windows. Use the nvm-windows alternative:
> 

### 🔧 Steps:

1. Go to the official `nvm-windows` GitHub repo:
    
    👉 https://github.com/coreybutler/nvm-windows
    
2. Download the **`nvm-setup.exe`** from the [Releases page](https://github.com/coreybutler/nvm-windows/releases).
3. Run the installer:
    - Choose install path (default is fine: `C:\Program Files\nvm`)
    - It will also create a symlink at `C:\Program Files\nodejs`
    - Let it update system PATH (recommended)

---

## ✅ 2. Verify Installation

After installation, open a new terminal (e.g., CMD or PowerShell) and run:

```bash
nvm version

```

You should see something like:

```bash
1.1.10

```

---

## ✅ 3. Install and Use Node.js Versions

### 🔽 Install a specific Node version

```bash
nvm install 18.17.1
nvm install 20.17.0

```

### ✅ Use a specific Node version

```bash
nvm use 20.17.0

```

You’ll see:

```bash
Now using node v20.17.0 (64-bit)

```

### 🧪 Check version in use:

```bash
node -v
npm -v

```

---

## ✅ 4. List and Remove Versions

### 📋 List installed Node versions:

```bash
nvm list

```

### ❌ Remove a Node version:

```bash
nvm uninstall 14.21.3

```

---

## ✅ 5. Set a Default Node Version

To set a default version (used every time the terminal opens):

```bash
nvm use 18.17.1

```

Then:

```bash
nvm alias default 18.17.1

```

---

## ✅ 6. Global `npm` Package Location

Each Node version installed by `nvm` has its **own global npm packages**.

To install a global package for the current Node version:

```bash
npm install -g nodemon

```

You must reinstall global packages for each Node version.

---

## 🧼 7. Troubleshooting Tips

- Always close and reopen terminal after switching versions
- Avoid installing Node directly from [https://nodejs.org](https://nodejs.org/) if using `nvm`
- Use `nvm root` to check where versions are installed

---

Let me know if you want a shell script, auto-switch `.nvmrc`, or how to use it with VS Code!