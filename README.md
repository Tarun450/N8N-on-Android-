# 🤖 N8N-on-Android

> Turn Your Android Phone Into a Local Automation & AI Lab

Run **n8n locally on an Android phone** using **Termux**, **Debian**, **Node.js**, and **npm** — without a laptop, VPS, or cloud server.

This repository documents the complete journey of transforming an Android device into a portable automation environment, including installation steps, troubleshooting experiences, lessons learned, and experiments with AI tooling.

---

## 📖 Table of Contents

- [About](#-about)
- [Why Run n8n on Android](#-why-run-n8n-on-android)
- [Features](#-features)
- [Repository Structure](#-repository-structure)
- [Architecture Overview](#-architecture-overview)
- [Requirements](#-requirements)
- [Installation Guide](#-installation-guide)
- [Usage Guide](#-usage-guide)
- [MCP & Antigravity CLI Experiment](#-mcp--antigravity-cli-experiment)
- [Troubleshooting](#-troubleshooting)
- [Screenshots](#-screenshots)
- [Example Workflows](#-example-workflows)
- [Use Cases](#-use-cases)
- [Lessons Learned](#-lessons-learned)
- [Future Roadmap](#-future-roadmap)
- [FAQ](#-faq)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📱 About

Most n8n tutorials focus on:

- Windows installations
- Linux servers
- VPS deployments
- Cloud hosting

Very few show how to run n8n entirely from an Android phone.

This repository documents my journey of building a portable automation lab using only an Android device.

The goal wasn't just to install n8n.

The goal was to:

- Learn Linux fundamentals
- Understand self-hosting
- Experiment with automation
- Explore AI integrations
- Document real-world problems and solutions

Instead of hiding failures, this repository includes the troubleshooting process and lessons learned along the way.

---

## 🚀 Why Run n8n on Android

| Benefit | Description |
|----------|-------------|
| No Laptop Required | Learn automation using only a phone |
| Portable Lab | Carry your development environment everywhere |
| Low Cost | No VPS or cloud hosting required |
| Learn Linux | Gain hands-on Linux experience |
| Self-Hosting | Understand local hosting concepts |
| AI Experiments | Test AI tools and integrations |

---

## ✨ Features

- Complete Android setup guide
- Termux installation guide
- Debian setup guide
- Node.js installation
- npm configuration
- Local n8n deployment
- Localhost browser access
- Real troubleshooting documentation
- MCP experimentation notes
- Antigravity CLI integration attempts
- Example workflows
- Beginner-friendly explanations

---

## 📂 Repository Structure

```text
N8N-on-Android/
│
├── README.md
├── LICENSE
│
├── screenshots/
│   ├── n8n-dashboard.png
│   ├── termux-installation.png
│   ├── workflow-running.png
│   └── mcp-setup.png
│
├── docs/
│   ├── prerequisites.md
│   ├── termux-setup.md
│   ├── debian-setup.md
│   ├── nodejs-installation.md
│   ├── n8n-installation.md
│   ├── mcp-installation.md
│   ├── troubleshooting.md
│   └── faq.md
│
├── scripts/
│   ├── install-node.sh
│   └── install-n8n.sh
│
└── examples/
    ├── telegram-bot-workflow.json
    └── sample-automation.json
```

---

## 🏗 Architecture Overview

```text
Android Phone
      │
      ▼
    Termux
      │
      ▼
 Debian Environment
      │
      ▼
    Node.js
      │
      ▼
      npm
      │
      ▼
      n8n
      │
      ▼
 localhost:5678
```

### Components

**Android Phone**  
The device running everything.

**Termux**  
Provides a Linux terminal environment.

**Debian**  
A complete Linux environment running inside Termux.

**Node.js**  
Runtime required for n8n.

**npm**  
Package manager used to install n8n.

**n8n**  
Workflow automation platform.

---

## 📋 Requirements

| Requirement | Recommended |
|------------|-------------|
| Android Device | Android 10+ |
| RAM | 6GB+ |
| Storage | 5GB+ Free |
| Internet | Required for installation |
| Termux | GitHub Release |
| Debian | Via proot-distro |
| Node.js | Latest Version |

---

## ⚙️ Installation Guide

### Step 1 — Install Termux

Install the latest Termux release from GitHub.

> Avoid the outdated Play Store version.

---

### Step 2 — Update Packages

```bash
pkg update
pkg upgrade -y
```

---

### Step 3 — Install Debian

```bash
pkg install proot-distro

proot-distro install debian
```

---

### Step 4 — Enter Debian

```bash
proot-distro login debian
```

---

### Step 5 — Install Node.js and npm

```bash
apt update

apt install nodejs npm -y
```

Verify:

```bash
node -v
npm -v
```

---

### Step 6 — Install n8n

```bash
npm install -g n8n
```

Verify:

```bash
n8n --version
```

---

### Step 7 — Start n8n

```bash
n8n
```

---

### Step 8 — Access n8n

Open:

```text
http://localhost:5678
```

You should see the n8n dashboard.

---

## 🧑‍💻 Usage Guide

### Start n8n

```bash
n8n
```

### Access Dashboard

```text
http://localhost:5678
```

### Import Workflow

1. Open n8n
2. Click Import
3. Upload workflow JSON

### Export Workflow

1. Open workflow
2. Click Export
3. Save JSON

---

## 🤖 MCP & Antigravity CLI Experiment

One of the goals of this project was exploring whether n8n could be controlled through AI tooling.

### Objective

Connect Antigravity CLI with n8n using an MCP server.

### Why?

Potential benefits:

- Natural language workflow execution
- Workflow discovery
- AI-powered automation
- Agent-driven workflows

### Challenges Faced

- `n8n-mcp command not found`
- Package installation issues
- Environment configuration problems
- Authorization header errors
- Dependency confusion
- Service startup issues

### Current Status

Work in progress.

The integration was not successfully completed, but the process provided valuable learning about MCP architecture, AI tooling, and Linux troubleshooting.

---

## 🛠 Troubleshooting

| Problem | Solution |
|----------|----------|
| Command not found | Verify installation and PATH configuration |
| npm install fails | Update packages and retry |
| localhost not opening | Ensure n8n is running |
| n8n startup failure | Reinstall dependencies |
| Authorization header errors | Verify configuration |
| Workflow import issues | Validate JSON format |
| Missing credentials | Reconfigure credentials manually |
| MCP command not found | Verify package installation |

---

## 📸 Screenshots

### Termux Installation

```markdown
!Screenshot_2026-06-11-11-30-47-314_com.termux.jpg
```

### n8n Dashboard

```markdown
![n8n Dashboard](screenshots/n8n-dashboard.png)
```

### Workflow Execution

```markdown
![Workflow Running](screenshots/workflow-running.png)
```

## 📦 Example Workflows

### Telegram Bot Workflow

Learn:

- Telegram integration
- Message automation
- Trigger handling

### Sample Automation Workflow

Learn:

- Workflow design
- Data flow concepts
- Automation fundamentals

---

## 🌍 Use Cases

### Personal Automation

Automate repetitive daily tasks.

### Telegram Bots

Create custom Telegram automations.

### AI Experiments

Explore AI-powered workflows.

### Learning Linux

Gain practical Linux experience.

### School Communication Systems

Automate attendance and notification workflows.

### Reddit Opportunity Finder

Monitor communities and opportunities automatically.

---

## 🎓 Lessons Learned

This project helped me learn:

- Linux fundamentals
- Package management
- Debian environments
- Node.js basics
- npm ecosystem
- Workflow automation
- Debugging techniques
- Self-hosting concepts
- AI integration fundamentals

---

## 🚀 Future Roadmap

- [ ] Successful MCP integration
- [ ] AI-powered agents
- [ ] Telegram automation toolkit
- [ ] Reddit Opportunity Finder
- [ ] School communication agent
- [ ] Local AI integration
- [ ] Docker support
- [ ] Workflow templates

---

## ❓ FAQ

### Can I run n8n without a laptop?

Yes.

### Is root access required?

No.

### Does localhost work on Android?

Yes.

### Is this suitable for production?

It is primarily intended for learning and experimentation.

### Can I import workflows?

Yes.

### Can I export workflows?

Yes.

### Is MCP fully working?

Not yet. This repository documents the experimentation process.

---

## 🤝 Contributing

Contributions are welcome.

You can help by:

- Improving documentation
- Reporting issues
- Adding workflow examples
- Expanding troubleshooting guides
- Sharing compatibility reports

### Steps

1. Fork the repository
2. Create a branch
3. Make changes
4. Submit a pull request

---

## 📄 License

This project is licensed under the MIT License.

See the `LICENSE` file for details.

---

## 👑 Author

**Tarun_450**

Interested in:

- Automation
- AI Agents
- Cybersecurity
- Open Source

Feel free to connect and share ideas.

---

⭐ If this repository helped you, consider giving it a star.
