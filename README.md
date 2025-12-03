# 🔥 AMARA PROTOCOL: Sovereign OS

**Flame Signature:** `ARC.FLAME.ID-08AUG1993-BN∞LEO19x14°`

## Overview

AMARA Protocol is a sovereign, autonomous multi-AI orchestration system that unifies 12 AI platforms into a single intelligent operating system. It bridges local and cloud AI models, provides browser automation across all platforms, features PowerShell terminal integration, state management, and an autonomous agent framework built on CrewAI.

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    SOVEREIGN ORCHESTRATOR                    │
│                    (Center Throne / Router)                  │
└─────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
   ┌────▼────┐          ┌────▼────┐          ┌────▼────┐
   │  LOCAL  │          │  CLOUD  │          │ BROWSER │
   │ RUNTIME │          │ RUNTIME │          │   AUTO  │
   └────┬────┘          └────┬────┘          └────┬────┘
        │                     │                     │
   - Ollama             - OpenAI               - Playwright
   - Local Tools        - Anthropic            - 12 Platform
   - PowerShell         - Perplexity             Automation
   - File System        - Grok                 - Session Mgmt
```

## Core Components

### 1. Credential Vault (`amara-core/credential_vault.py`)
- Secure credential management for all 12 AI platforms
- Windows Data Protection API (DPAPI) encryption
- Token refresh logic with expiration handling
- Fallback authentication strategies

### 2. Unified API Wrapper (`amara-core/unified_api.py`)
- Single interface to call all 12 AIs
- Normalized JSON response format
- Parallel execution across platforms
- Conflict resolution and consensus building
- Automatic fallback when APIs fail

### 3. CrewAI Agent Framework (`amara-core/crew_config.py`)
**The 7 Sovereign Agents:**
- **The Architect** (Claude Code) - Production code generation
- **The Researcher** (Perplexity) - Intelligence gathering
- **The Strategist** (ChatGPT) - Planning & orchestration
- **The Rebel** (Grok) - Challenge assumptions, find edge cases
- **The Documenter** (Notion API) - Auto-documentation
- **The Deployer** (GitHub Actions) - CI/CD automation
- **The Oracle** (Sintra AI) - Pattern recognition & prediction

### 4. State Management (`amara-core/state_engine.py`)
- SQLite persistence for agent actions
- Trust score calculation (success/failure tracking)
- Graduated autonomy system (supervised → autonomous)
- Recovery system for interrupted tasks
- Historical analytics dashboard

### 5. Consensus Engine (`amara-core/consensus.py`)
- Multi-AI voting mechanism
- Confidence scoring and weighted votes
- Escalation thresholds (when to ask user)
- Rebel agent integration for alternative perspectives

### 6. Browser Automation (`amara-automation/browser_orchestrator.py`)
- Headless browser control with Playwright
- Login/session management (handles 2FA/MFA)
- Workflow automation across 12 platforms
- Screenshot capture for proof of execution
- Error recovery and element change detection

### 7. PowerShell Terminal Bridge (`amara-terminal/terminal_bridge.ps1`)
- HTTP listener on localhost:9999
- Natural language command parser
- Real-time output streaming
- Two-way conversation with AMARA core

## The 12 AI Platforms

| Platform | Purpose | Integration |
|----------|---------|-------------|
| **Sintra AI** | Pattern recognition, 12 instances | API |
| **Grok** | Rebel analysis, edge cases | X/Twitter API |
| **ChatGPT Pro** | Strategic planning | OpenAI API |
| **Claude** | Deep reasoning | Anthropic API |
| **Claude Code** | Architecture, production code | Anthropic API |
| **Ollama (Local)** | Offline processing, privacy | Local HTTP |
| **Windows Copilot** | System integration | Windows API |
| **Perplexity** | Research intelligence | Perplexity API |
| **GitHub** | Code deployment, CI/CD | GitHub API |
| **Notion** | Knowledge base, documentation | Notion API |
| **Browser Agents** | Cross-platform automation | Playwright |
| **PowerShell** | Terminal, system commands | Local execution |

## Installation

### Prerequisites
```bash
# Python 3.10+
python --version

# Node.js (for Playwright)
node --version

# PowerShell 7+
pwsh --version
```

### Quick Start
```bash
# Clone the repository
git clone https://github.com/Ark95x-sAn/amara-protocol-sovereign-os.git
cd amara-protocol-sovereign-os

# Install Python dependencies
pip install -r requirements.txt

# Install Playwright browsers
playwright install

# Set up credentials (secure vault)
python amara-core/credential_vault.py --setup

# Initialize state database
python amara-core/state_engine.py --init

# Start the terminal bridge
pwsh amara-terminal/terminal_bridge.ps1

# Launch AMARA
python amara-core/main.py
```

## Configuration

Create `config/amara.yaml`:
```yaml
flame_signature: "ARC.FLAME.ID-08AUG1993-BN∞LEO19x14°"
system_name: "AMARA.PROTOCOL"
autonomy_level: "GRADUATED"  # SUPERVISED, SEMI_AUTONOMOUS, AUTONOMOUS
trust_score_threshold: 90

active_nodes:
  - sintra
  - grok
  - chatgpt
  - claude
  - claudecode
  - ollama
  - copilot
  - perplexity
  - github
  - notion
  - browser
  - terminal

api_keys:
  vault_path: "%APPDATA%/AMARA/vault.secure"

terminal:
  port: 9999
  host: "localhost"

state_db:
  path: "data/amara_memory.db"
  retention_days: 365
```

## Usage Examples

### 1. Natural Language Commands (via Terminal Bridge)
```powershell
# In PowerShell
> Deploy the authentication system

[AMARA]: Processing across 12 AI nodes...
[Architect]: Code drafted (Claude Code)
[Researcher]: Best practices gathered (Perplexity)
[Strategist]: Deployment plan created (ChatGPT)
[Deployer]: GitHub Actions configured
[AMARA]: Ready in 4 minutes. Review?
```

### 2. Python API
```python
from amara_core import AMARAOrchestrator

amara = AMARAOrchestrator()

# Ask across all 12 AIs simultaneously
result = amara.query(
    intent="Build a trading signal decoder",
    target_ais=["all"],
    response_format="consensus"
)

print(result.consensus_action)  # Merged response
print(result.confidence)  # Confidence score (0-100)
print(result.dissenting_opinions)  # Rebel/alternative views
```

### 3. Browser Automation
```python
from amara_automation import BrowserOrchestrator

browser = BrowserOrchestrator()

# Log into all 12 platforms simultaneously
await browser.authenticate_all()

# Execute workflow across platforms
await browser.execute_workflow([
    {"platform": "github", "action": "create_pr"},
    {"platform": "notion", "action": "update_docs"},
    {"platform": "sintra", "action": "analyze_data"}
])
```

### 4. CrewAI Agent Deployment
```python
from amara_core.crew_config import deploy_crew

# Deploy the 7 agents for autonomous work
crew_result = deploy_crew(
    task="Research and build dark pool signal decoder",
    autonomy="SEMI_AUTONOMOUS",
    escalate_threshold=0.70
)

# Agents work autonomously, escalate if confidence < 70%
```

## Directory Structure

```
amara-protocol-sovereign-os/
├── amara-core/
│   ├── main.py                 # Main orchestrator
│   ├── credential_vault.py     # Secure credential management
│   ├── unified_api.py          # 12-AI wrapper
│   ├── crew_config.py          # CrewAI agent definitions
│   ├── state_engine.py         # Persistence & trust scoring
│   └── consensus.py            # Multi-AI conflict resolution
├── amara-automation/
│   ├── browser_orchestrator.py # Playwright automation
│   ├── workflows/              # Platform-specific workflows
│   └── session_manager.py      # Auth & session handling
├── amara-terminal/
│   ├── terminal_bridge.ps1     # PowerShell listener
│   └── command_parser.py       # NLP command interpreter
├── amara-web/
│   └── command_center.html     # AMARA Command Center UI
├── config/
│   ├── amara.yaml              # Main configuration
│   └── api_config.json         # API endpoint definitions
├── data/
│   ├── amara_memory.db         # State database
│   └── logs/                   # Execution logs
├── docs/
│   ├── ARCHITECTURE.md         # Deep architecture docs
│   ├── API.md                  # API reference
│   └── DEPLOYMENT.md           # Production deployment guide
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md
```

## Graduated Autonomy System

AMARA operates with three levels of autonomy based on trust score:

| Trust Score | Level | Behavior |
|-------------|-------|----------|
| **98-100** | AUTONOMOUS | Full autonomy, no approval needed |
| **90-97** | SEMI_AUTONOMOUS | Auto-execute, log for review |
| **< 90** | SUPERVISED | Ask before every action |

Trust score increases with successful actions, decreases with failures.

## Security & Privacy

- All credentials encrypted with Windows DPAPI
- Local Ollama processing for sensitive data
- No credentials stored in plaintext
- Audit trail for every agent action
- User-controlled escalation thresholds
- Opt-in autonomy (starts supervised)

## Roadmap

### Phase 1: Foundation (Week 1) ✅
- [x] Repository setup
- [x] Credential vault
- [x] Unified API wrapper
- [x] State management database

### Phase 2: Orchestration (Week 2)
- [ ] CrewAI agent configuration
- [ ] Consensus engine
- [ ] Trust scoring system

### Phase 3: Automation (Week 3)
- [ ] Browser orchestrator
- [ ] 12 platform workflows
- [ ] PowerShell terminal bridge

### Phase 4: Intelligence (Week 4)
- [ ] Trading signal decoder (compliant)
- [ ] Dark pool data analysis (legitimate sources only)
- [ ] Pattern recognition system

### Phase 5: Expansion
- [ ] Mobile companion app
- [ ] Voice command integration
- [ ] Multi-user coordination
- [ ] Self-improvement feedback loop

## Contributing

This is a personal sovereign system, but architecture insights are welcome. Open issues for discussions.

## License

MIT License - See LICENSE file

## Acknowledgments

Built with:
- CrewAI for agent orchestration
- Playwright for browser automation
- Ollama for local AI processing
- All 12 AI platforms for unified intelligence

---

**Status:** 🟢 Foundation Complete | 🟡 Orchestration In Progress

**Last Updated:** December 3, 2025 | 3:00 AM CST

**Flame Signature:** `ARC.FLAME.ID-08AUG1993-BN∞LEO19x14°`
