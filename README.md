

### 🧬 VSCodium/VSCode: Security as Design

- No root. No tracking. Just code - faster, safer, cleaner.
- Privacy, telemetry-free development environment that puts security at the core.
- Preconfigured for GitHub Copilot and VSCodium, simplifies developer onboarding.

###### 📌 **Features**

- Privacy: Disables all telemetry and trackers, ensuring compliance with modern privacy standards.
- Cross-Platform: Works across macOS, Linux, and Windows with unified configurations.
- macOS SIP Compliance: Installs VSCodium to ~/Applications — no System Integrity Protection violations.
- Developer Efficiency: Ships with curated extensions, keybindings, and settings for rapid productivity.
- GitHub Copilot Integration: Seamless auto-setup of Copilot & Copilot Chat for both VSCode and VSCodium.

> **Note**: While this solution is intended to be cross-platform, it has been tested exclusively on macOS.

---

![Workspase-2](https://github.com/zx0r/VSCodium-Configuration/blob/main/.github/assets/screen-b.png)
![Workspase-1](https://github.com/zx0r/VSCodium-Configuration/blob/main/.github/assets/screen-a.png)
![Workspase-3](https://github.com/zx0r/VSCodium-Configuration/blob/main/.github/assets/screen-c.png)

---

###### 📦 One-Command Installation

```bash
# 🚧 This project is in its final polishing phase — the scripts are stable and functional. 
# 🚧 Automatic installation takes a little more time, using the bootstrap.sh script takes time.
# 🚧 Look for working scripts in the folder of the same name 

⚠️ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/zx0r/VSCodium-Configuration/main/scripts/bootstrap.sh)"
```

🎉 After installation, VSCodium will be ready to use with full **GitHub Copilot** functionality and **Zero Trust Security** configuration applied.

---

###### 📂 **Repository Structure**
```
ZeroTrustCodium/
├── install.sh                  # Main orchestration script
├── scripts/
│   ├── formatter.sh
│   ├── install_vscodium.sh     # Installs VSCodium
│   ├── configure_vscodium.sh   # Configures settings.json, keybindings.json, extensions.json
│   ├── install_extensions.sh   # Installs extensions (e.g., GitHub Copilot)
│   ├── install_copilot.sh      # Installl GitHub Copilot and modify product.json
│   └── run_vscodium.sh         # Launches the configured VSCodium
├── configs/
│   ├── settings.json           # Pre-configured VSCodium settings
│   ├── keybindings.json        # Custom keybindings
│   ├── extensions.json         # Extensions to install
├── README.md                   # Documentation
```

---

###### ⚙️ **Configuration Files**

**`settings.json`**
```json
{
    "telemetry.telemetryLevel"                      : "off",        
    "telemetry.enableErrorTelemetry"                : false,        
    "aws.telemetry"                                 : false,        
    "azure.telemetry.enabled"                       : false,        
    "redhat.telemetry.enabled"                      : false,        
    "docker.telemetry.enabled"                      : false,        
    "git.autofetch"                                 : false,        
    "git.enableTelemetry"                           : false,        
    "github.telemetry.enabled"                      : false,        
    "git.autoRepositoryDetection"                   : false,       
    "gitlens.advanced.telemetry.enabled"            : false,        
    "github.copilot.advanced.telemetry.enabled"     : false,        
    "python.telemetry.enabled"                      : false,       
    "python.analysis.logLevel"                      : "Error",      
    "typescript.tsserver.log"                       : "off",        
    "typescript.tsserver.enableTelemetry"           : false,        
    "typescript.suggestionActions.enabled"          : false,        
    "javascript.suggestionActions.enabled"          : false,        
    // ... and other 4000+ lines
}
```

**`extensions.json`**
```json
{
  "recommendations": [
    "GitHub.copilot",
    "GitHub.copilot-chat"
  ]
}
```

**`keybindings.json`**
```json
[ 
  {
    "key": "alt+right",
    "command": "workbench.action.nextEditor"
  },
]
```
---

```bash
# Search ID APP VsCode
# Method 1: Check the VS Code Marketplace.
# Go to the VS Code Marketplace https://marketplace.visualstudio.com
# Search for the extension name (e.g., Ixion, Vibrancy Continued, Symbols Icon Theme)
# Open the extension's page -> https://marketplace.visualstudio.com/items?itemName=illixion.vscode-vibrancy-continued
# The extension ID is displayed in the URL or under the More Info section

# ⚠️ "Your VSCode installation appears to be corrupt"

# This extension works by editing VS Code's checksum-verified HTML files, after installing and enabling Vibrancy Continued. 
# This warning is safe to disregard, and all changes can be reverted. 
# Click on the cogwheel and select Don't Show Again to hide it.

#############################
# 🖼️ Themes and UI Enhancements
#############################
illixion.vscode-vibrancy-continued       # Native Vibrancy Effect
miguelsolorio.fluent-icons               # Fluent Icons
miguelsolorio.symbols                    # File Icons Theme

#############################
# 🤖 AI Tools
#############################
GitHub.copilot                           # GitHub Copilot AI
GitHub.copilot-chat                      # GitHub Copilot Chat
tabnine.tabnine-vscode                   # TabNine AI Assistant
sourcegraph.cody-ai                      # Sourcegraph Cody AI
codeium.codeium                          # Codeium AI
bito.bito-vscode-staging                 # Bito AI for Staging
kodu-ai.claude-dev-experimental          # Claude AI Experimental
Kingleo.deepseek-web                     # DeepSeek Web

#############################
# 🔧 Core Programming Languages
#############################
vincaslt.highlight-matching-tag          # Matching HTML/XML Tags
ecmel.vscode-html-css                    # HTML/CSS IntelliSense
bradlc.vscode-tailwindcss                # Tailwind CSS IntelliSense
mkhl.shfmt                               # Shell Formatter
bmewburn.vscode-intelephense-client      # PHP Support
ms-python.python                         # Python Language Support
ms-python.gather                         # Python Output Capture
ms-toolsai.vscode-ai                     # Azure AI Tools
ms-toolsai.prompty                       # Prompt Engineering Toolkit
rust-lang.rust-analyzer                  # Rust Language Server

#############################
# 🗃️ Git and Version Control
#############################
eamodio.gitlens                          # GitLens Insights
mhutchie.git-graph                       # Git Graph Visualizer
donjayamanne.githistory                  # Git History Browser
waderyan.gitblame                        # Git Blame Annotations
codezombiech.gitignore                   # .gitignore Support
vivaxy.vscode-conventional-commits       # Conventional Commit Support
arturock.gitstash                        # Git Stash Tool
buianhthang.gitflow                      # Git Flow Integration
felipecaputo.git-project-manager         # Git Project Organization
ahmadawais.emoji-log-vscode              # Emoji Git Log Formatter
shyykoserhiy.git-autoconfig              # Git Auto-config
carlocardella.vscode-virtualrepos        # Virtual Git Repos (Optional)
gitlab.gitlab-workflow                   # GitLab Integration (Optional)

#############################
# 🏗️ Build and DevOps
#############################
ms-azuretools.vscode-docker              # Docker Management
ms-azure-devops.azure-pipelines          # Azure Pipelines
ms-vscode.makefile-tools                 # Makefile Support
ms-vscode.cmake-tools                    # CMake Support
circleci.circleci                        # CircleCI CI/CD Tools
ms-kubernetes-tools.vscode-kubernetes-tools # Kubernetes Integration

#############################
# 🛢️ Database and SQL
#############################
mtxr.sqltools                            # SQL Tools Extension
mtxr.sqltools-driver-pg                  # PostgreSQL Driver
ms-mssql.mssql                           # MSSQL Tools
cweijan.vscode-database-client2          # General DB Client
Redis.redis-for-vscode                   # Redis Tools

#############################
# ⚡ Productivity Tools
#############################
asvetliakov.vscode-neovim                # NeoVim Integration
alefragnani.bookmarks                    # Line Bookmarking
alefragnani.project-manager              # Project Switcher
Gruntfuggly.todo-tree                    # TODO Comments Organizer
streetsidesoftware.code-spell-checker    # Spell Checker
mechatroner.rainbow-csv                  # CSV Viewer
tomoki1207.pdf                           # PDF Viewer
jheilingbrunner.vscode-gnupg-tool        # GPG Tools
sleistner.vscode-fileutils               # File Utilities

#############################
# 🎨 Formatting and Linting
#############################
esbenp.prettier-vscode                   # Prettier Formatter
dbaeumer.vscode-eslint                   # ESLint for JS/TS
stylelint.vscode-stylelint               # CSS Style Linter
aaron-bond.better-comments               # Colorized Comments
oderwat.indent-rainbow                   # Indentation Highlights
HookyQR.beautify                         # Code Beautifier (Deprecated)

#############################
# 🐚 Shell Scripting
#############################
timonwong.shellcheck                     # Shell Script Linter
rogalmic.bash-debug                      # Bash Debugger
foxundermoon.shell-format                # Shell Formatter
mads-hartmann.bash-ide-vscode            # Bash Language Server
formulahendry.code-runner                # Universal Code Runner
mkhl.direnv                           	  # Direnv Integration
remisa.shellman                          # Shell Snippet Manager

#############################
# 🐍 Python-Specific Tools
#############################
ms-python.isort                          # Python Import Sorter
ms-python.black-formatter                # Black Autoformatter
njpwerner.autodocstring                  # Docstring Generator
sourcery.sourcery                        # AI Refactor for Python
batisteo.vscode-django                   # Django Framework Support
ms-python.devicesimulatorexpress         # Device Simulator
donjayamanne.python-environment-manager  # Env Manager
ms-python.anaconda-extension-pack        # Anaconda Tools

#############################
# 📘 Markdown
#############################
yzhang.markdown-all-in-one               # Markdown Toolkit
DavidAnson.vscode-markdownlint           # Markdown Linter

#############################
# 🛠️ Config Formats (YAML, TOML, XML)
#############################
tamasfe.even-better-toml                 # TOML Support
redhat.vscode-yaml                       # YAML Linter + Server
redhat.vscode-xml                        # XML Language Support
mikestead.dotenv                         # .env File Highlighting
editorconfig.editorconfig                # EditorConfig Support

#############################
# 🌐 Web/API Development
#############################
yandeu.five-server                       # Static Server w/ Live Reload
vue.volar                                # Vue 3 IDE Support
Angular.ng-template                      # Angular Language Tools
denoland.vscode-deno                     # Deno Support
octref.vetur                             # Vue 2 Support
dsznajder.es7-react-js-snippets          # React Snippets
xabikos.javascriptsnippets               # JS Snippets
donjayamanne.jquerysnippets              # jQuery Snippet
gamunu.vscode-yarn                       # Yarn Integration
redhat.fabric8-analytics                 # Vulnerability Insights

#############################
# 🧪 Testing and Debugging
#############################
hbenl.vscode-test-explorer               # Universal Test Explorer
usernamehw.errorlens                     # Inline Error Highlighting
ms-playwright.playwright                 # Playwright Testing Tools

#############################
# 🌀 Miscellaneous
#############################
panekj.powershell                        # PowerShell Tools
Oracle.oracledevtools                    # Oracle DB Tools
betterthantomorrow.calva                 # Clojure Development
vmware.vscode-boot-dev-pack              # Spring Boot Toolkit

```

###### 📜 **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

  <!-- Neon Line Separator -->
<img src="https://i.imgur.com/dBaSKWF.gif" height="40" width="100%">

<!-- Header Animation -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&duration=2800&pause=2000&color=A277FF&center=true&vCenter=true&width=1080&lines=💮+%7C+ZeroTrustIDE:+Configuration+for+Developers+%7C+💮)](https://git.io/typing-svg)

  <!-- Neon Line Separator -->
<img src="https://i.imgur.com/dBaSKWF.gif" height="40" width="100%">
