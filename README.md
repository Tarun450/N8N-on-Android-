
🤖 n8n-on-android
Turn Your Android Phone Into a Local Automation & AI Lab
� � � � � �
Run n8n locally on an Android phone using Termux, Debian, Node.js, and npm—without a laptop, cloud server, or paid hosting.
This repository documents the complete journey of transforming an Android device into a portable automation lab, including the installation process, troubleshooting experience, lessons learned, and experiments with AI tooling and MCP integrations.
📚 Table of Contents
About The Project
Why Run n8n on Android?
Features
Repository Structure
Architecture Overview
Requirements
Installation Guide
Usage Guide
MCP & Antigravity CLI Experiment
Troubleshooting
Screenshots
Example Workflows
Use Cases
Lessons Learned
What Makes This Repository Different?
Learning Outcomes
Future Improvements
FAQ
Contributing
Best Practices
Security Notes
License
Author
🚀 About The Project
Most tutorials focus on:
Windows installations
Linux servers
VPS deployments
Cloud hosting
Very few show how to run n8n entirely from an Android phone.
This repository exists to bridge that gap.
The goal was simple:
Build a portable automation environment using only an Android device.
During this journey, I learned Linux fundamentals, package management, local hosting, workflow automation, debugging, and AI integration concepts.
Instead of documenting only the successful steps, this repository also covers the mistakes, failures, and troubleshooting process so others can learn faster.
📱 Why Run n8n on Android?
Benefit
Description
No Laptop Required
Learn automation using only a phone
Portable Lab
Carry your development environment everywhere
Low Cost
No VPS or cloud server needed
Self-Hosted Learning
Understand local hosting concepts
AI Experiments
Explore AI agents and integrations
Linux Practice
Learn Linux through hands-on experience
Perfect For
✅ Students
✅ Automation Beginners
✅ AI Enthusiasts
✅ Self-Hosting Learners
✅ Mobile-First Developers
✨ Features
[x] Complete Android setup guide
[x] Termux installation guide
[x] Debian environment setup
[x] Node.js installation
[x] npm setup
[x] Local n8n deployment
[x] Browser access via localhost
[x] Real troubleshooting documentation
[x] MCP integration experiments
[x] Antigravity CLI experimentation
[x] Example workflow collection
[x] Beginner-friendly explanations
[x] Learning resources
[x] Future AI roadmap
📂 Repository Structure
Plain text
n8n-on-android/
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
🏗 Architecture Overview
Plain text
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
Browser (localhost:5678)
Simple Explanation
Android Phone
The physical device running everything.
Termux
Provides a Linux-like terminal environment on Android.
Debian
Creates a more complete Linux environment inside Termux.
Node.js
Runs JavaScript applications.
npm
Installs and manages packages.
n8n
The workflow automation platform.
Browser
Access the n8n dashboard through localhost.
📋 Requirements
Requirement
Recommended
Android Device
Android 10+
RAM
6GB+
Storage
5GB+ Free
Internet
Required for installation
Termux
Latest GitHub Release
Debian
Via proot-distro
Node.js
Latest LTS
npm
Included with Node.js
⚙️ Installation Guide
Step 1 — Install Termux
Download Termux from GitHub Releases.
⚠️ Avoid outdated Play Store versions.
Step 2 — Update Packages
Bash
pkg update
pkg upgrade -y
Step 3 — Install Debian
Bash
pkg install proot-distro

proot-distro install debian
Step 4 — Enter Debian
Bash
proot-distro login debian
Step 5 — Install Node.js & npm
Bash
apt update

apt install nodejs npm -y
Verify installation:
Bash
node -v

npm -v
Step 6 — Install n8n
Bash
npm install -g n8n
Verify installation:
Bash
n8n --version
Step 7 — Start n8n
Bash
n8n
Step 8 — Open n8n
Visit:
Plain text
http://localhost:5678
You should see the n8n dashboard.
🎉 Congratulations! Your Android phone is now running n8n locally.
🧑‍💻 Usage Guide
Start n8n
Bash
n8n
Access Dashboard
Plain text
http://localhost:5678
Create Workflows
Add nodes
Configure triggers
Connect actions
Execute workflows
Import Workflow
Open n8n
Click Import
Upload JSON file
Export Workflow
Open workflow
Click Export
Save JSON
🤖 MCP & Antigravity CLI Experiment
Goal
Connect Antigravity CLI with n8n through an MCP server.
The vision was:
Plain text
Antigravity CLI
        │
        ▼
     MCP Server
        │
        ▼
        n8n
        │
        ▼
   Workflow Control
Why MCP?
MCP (Model Context Protocol) enables AI tools to interact with external systems and applications.
Potential benefits:
Workflow execution
Workflow discovery
AI-powered automation
Natural language control
What Was Attempted?
Researching n8n MCP solutions
Installing MCP-related packages
Testing integrations
Connecting Antigravity CLI
Challenges Encountered
❌ n8n-mcp command not found
❌ Package installation issues
❌ Environment configuration challenges
❌ Authentication difficulties
❌ Service discovery problems
Lessons Learned
Even though the integration wasn't completed, the process provided valuable knowledge about:
MCP architecture
AI tooling
Linux troubleshooting
npm ecosystem
Service management
🛠 Troubleshooting
Problem
Possible Cause
Solution
Command not found
PATH issue
Reinstall package and verify installation
npm install fails
Network or dependency issue
Retry installation and update packages
localhost not opening
n8n not running
Restart n8n
Authorization header errors
Configuration issue
Verify credentials and settings
Workflow import failure
Invalid JSON
Validate workflow file
Credentials missing
Imported workflow references missing credentials
Reconfigure credentials manually
MCP command not found
Package issue
Verify installation method
Debian won't start
Incomplete installation
Reinstall Debian
Node.js missing
Installation failed
Reinstall Node.js
n8n crashes
Dependency issue
Reinstall n8n
📸 Screenshots
Termux Installation
Plain text
screenshots/termux-installation.png
�
n8n Dashboard
Plain text
screenshots/n8n-dashboard.png
�
Workflow Running
Plain text
screenshots/workflow-running.png
�
📦 Example Workflows
Telegram Bot Workflow
Learn:
Telegram integration
Message automation
Trigger handling
Sample Automation Workflow
Learn:
Basic workflow design
Data flow concepts
Automation fundamentals
🌍 Real-World Use Cases
Personal Automation
Automate repetitive daily tasks.
Telegram Bots
Create and manage Telegram automations.
AI Agents
Experiment with AI-powered workflows.
Learning Linux
Practice Linux commands and package management.
School Communication Systems
Automate attendance and result notifications.
Reddit Opportunity Finder
Monitor communities and discover opportunities automatically.
Business Automation
Automate forms, notifications, and reports.
🎓 Lessons Learned
Through this project, I learned:
Linux fundamentals
Package management
Debian environments
Node.js basics
npm ecosystem
Local hosting
Workflow automation
Debugging techniques
AI integration concepts
Self-hosting principles
⭐ What Makes This Repository Different?
Typical Tutorials
This Repository
Windows setup
Android setup
Linux server setup
Mobile-first workflow
Cloud deployment
Local phone deployment
Ideal scenarios
Real troubleshooting
Basic installation
Complete learning journey
Success only
Successes and failures
No AI experiments
MCP & AI exploration
🎯 Learning Outcomes
After completing this guide, you'll understand:
How local hosting works
How n8n operates
Linux fundamentals
Debian environments
npm package management
Workflow automation
Debugging workflows
Self-hosted software deployment
🚀 Future Improvements
[ ] Successful MCP integration
[ ] AI agent workflows
[ ] Telegram automation toolkit
[ ] Reddit Opportunity Finder
[ ] School communication agent
[ ] Local AI model integration
[ ] Docker support
[ ] Mobile dashboard optimizations
[ ] Workflow template library
❓ FAQ
Can I run n8n without a laptop?
Yes.
Is root required?
No.
Does this work offline?
After installation, many workflows can run locally.
Is Android powerful enough?
For learning and small automations, absolutely.
Is this production-ready?
Primarily intended for learning and experimentation.
Can I use Telegram bots?
Yes.
Does localhost work on Android?
Yes.
Is Debian required?
Recommended.
Can I use another Linux distro?
Possibly.
Is n8n free?
Yes.
Does MCP work?
Work in progress.
Can I install AI tools?
Yes.
Is cloud hosting required?
No.
Can workflows be exported?
Yes.
Can workflows be imported?
Yes.
🤝 Contributing
Contributions are welcome.
You can help by:
Improving documentation
Reporting issues
Adding workflows
Improving troubleshooting guides
Sharing Android compatibility reports
Steps:
Fork repository
Create branch
Make changes
Submit pull request
💡 Best Practices
Keep backups of workflows.
Export important automations regularly.
Update packages carefully.
Document configuration changes.
Test workflows before production use.
Store credentials securely.
🔐 Security Notes
Keep credentials private.
Avoid sharing exported credential data.
Backup workflows frequently.
Review third-party packages before installation.
📄 License
Distributed under the MIT License.
See the LICENSE file for more information.
👑 Author
Tarun_450
Passionate about:
Automation
AI Agents
Open Source
🏷 GitHub Topics
Plain text
n8n
automation
termux
android
nodejs
workflow-automation
self-hosted
ai
open-source
mcp
mobile-development
debian
local-hosting
⭐ If this repository helped you turn your Android phone into an automation lab, consider giving it a star and sharing it with others. :::
