<div align="center">

<!-- Title with Gradient Effect -->
<h1>
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" alt="divider"/>
  <br/>
  🌌 Asteroid
  <br/>
  <sub>Orchestrate 50+ AI Agents to Automate Complex Research, Analysis & Workflows</sub>
  <br/>
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" alt="divider"/>
</h1>

<!-- Animated Badges -->
<p align="center">
  <img src="https://img.shields.io/badge/Version-0.0.1-00ADD8.svg?style=for-the-badge&logo=semanticrelease&logoColor=white" alt="Version"/>
  <img src="https://img.shields.io/badge/Python-3.12+-3776AB.svg?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/License-Apache%202.0-FF6B35.svg?style=for-the-badge&logo=apache&logoColor=white" alt="License"/>
  <img src="https://img.shields.io/badge/AI-Powered-9B59B6.svg?style=for-the-badge&logo=openai&logoColor=white" alt="AI"/>
  <img src="https://img.shields.io/badge/Status-Active-2ECC71.svg?style=for-the-badge" alt="Status"/>
</p>

<!-- Project Description with Animation Effect -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=3000&pause=1000&color=00D9FF&center=true&vCenter=true&multiline=true&width=700&height=80&lines=Orchestrate+50%2B+AI+agents+seamlessly;Transform+complex+tasks+into+intelligent+workflows;From+research+to+automation+in+minutes" alt="Typing SVG" />
</p>

<!-- Navigation Menu -->
<p align="center">
  <a href="#-features"><kbd><strong>🎯 Features</strong></kbd></a> •
  <a href="#-execution-modes"><kbd><strong>🔀 Modes</strong></kbd></a> •
  <a href="#-quick-start"><kbd><strong>⚡ Quick Start</strong></kbd></a> •
  <a href="#-architecture"><kbd><strong>🏗️ Architecture</strong></kbd></a> •
  <a href="#-documentation"><kbd><strong>📚 Docs</strong></kbd></a>
</p>

<br/>

<!-- Project Demo GIF or Screenshot Placeholder -->
<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://via.placeholder.com/800x400/1a1a1a/00D9FF?text=Asteroid+AI+Platform">
    <source media="(prefers-color-scheme: light)" srcset="https://via.placeholder.com/800x400/ffffff/0066CC?text=Asteroid+AI+Platform">
    <img alt="Asteroid Dashboard" src="https://via.placeholder.com/800x400/ffffff/0066CC?text=Asteroid+AI+Platform" style="max-width: 100%; border-radius: 10px; box-shadow: 0 8px 16px rgba(0,0,0,0.2);">
  </picture>
</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

</div>

<br/>

## 🌟 Overview

**Asteroid** is an advanced AI orchestration platform that coordinates **50+ specialized AI agents** to autonomously handle complex research, data analysis, and automation workflows. Built on the powerful [AG2](https://github.com/ag2ai/ag2) (AutoGen 2) framework, Asteroid transforms natural language prompts into sophisticated multi-agent collaborations that deliver enterprise-grade results—from comprehensive market research and scientific literature reviews to automated code generation and strategic planning.

<br/>

### ✨ Key Highlights

<table>
<tr>
<td width="50%" valign="top">

#### 🧩 **Composable Architecture**
```mermaid
graph LR
    A[Task Input] --> B{Mode Selection}
    B --> C[50+ Agents]
    C --> D[Orchestration]
    D --> E[Output]
    style A fill:#00D9FF
    style E fill:#2ECC71
```
- 🎯 **8 execution modes** for different workflows
- 🤖 **50+ specialized agents** with distinct roles
- 🔧 **Mix and match** to build custom pipelines
- 📦 **Pre-built templates** for common use cases

</td>
<td width="50%" valign="top">

#### 🔄 **Intelligent Orchestration**
```mermaid
graph TD
    A[Task] --> B[Planner]
    B --> C[Execution]
    C --> D[Validation]
    D --> E{Approved?}
    E -->|Yes| F[Complete]
    E -->|No| C
    style F fill:#2ECC71
```
- 💾 **Context preservation** across interactions
- 👤 **Human-in-the-loop** approval checkpoints
- ⚔️ **Adversarial validation** for stress-testing
- 📡 **Real-time monitoring** with WebSocket streaming

</td>
</tr>
</table>

<br/>

### 🎯 Why Choose Asteroid?

<div align="center">

| Feature | Benefit |
|:--------|:--------|
| 🚀 **Production Ready** | FastAPI backend with full REST API, Docker deployment |
| 🎨 **Modern UI** | Next.js 14 frontend with real-time updates and DAG visualization |
| 🔌 **Pluggable Tools** | CrewAI & LangChain integration with 30+ built-in tools |
| 🌐 **Multi-LLM Support** | OpenAI, Anthropic, Google Gemini, Mistral, and more |
| 📊 **Cost Tracking** | Comprehensive logging and token usage monitoring |
| 🗃️ **Data Persistence** | SQLAlchemy ORM with SQLite/PostgreSQL support |

</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🔀 Execution Modes

Asteroid provides **8 composable execution modes** that define how agents approach tasks:

<details open>
<summary><h3>📋 Complete Mode Reference</h3></summary>

<br/>

<table>
<tr>
<th width="20%">Mode</th>
<th width="40%">Description</th>
<th width="40%">Best For</th>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/🎯-Single--Pass-00D9FF?style=for-the-badge" alt="one-shot"/>
  <br/><code>one-shot</code>
</td>
<td>Direct execution with one agent, one pass. No planning overhead.</td>
<td>
  • Quick analysis<br/>
  • Code generation<br/>
  • Report drafts<br/>
  • Release notes
</td>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/🧭-Multi--Step-3498DB?style=for-the-badge" alt="planning"/>
  <br/><code>planning-control</code>
</td>
<td>Planner → Reviewer → Execution with context flow across phases.</td>
<td>
  • Market research<br/>
  • Competitive intelligence<br/>
  • Multi-part analyses<br/>
  • Strategic planning
</td>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/💡-Hypothesis-9B59B6?style=for-the-badge" alt="idea"/>
  <br/><code>idea-generation</code>
</td>
<td>Adversarial loop: idea_maker vs idea_hater for robust ideation.</td>
<td>
  • Product brainstorming<br/>
  • Strategic planning<br/>
  • Research directions<br/>
  • Innovation workshops
</td>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/📄-OCR-E74C3C?style=for-the-badge" alt="ocr"/>
  <br/><code>ocr</code>
</td>
<td>Mistral OCR for PDFs, scans, and handwritten notes extraction.</td>
<td>
  • Document digitization<br/>
  • Table extraction<br/>
  • Form processing<br/>
  • Archive scanning
</td>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/📚-Literature-F39C12?style=for-the-badge" alt="arxiv"/>
  <br/><code>arxiv</code>
</td>
<td>Paper download, content extraction, and intelligent summarization.</td>
<td>
  • Literature reviews<br/>
  • Research surveys<br/>
  • Bibliography generation<br/>
  • Academic analysis
</td>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/🔍-Enrichment-1ABC9C?style=for-the-badge" alt="enhance"/>
  <br/><code>enhance-input</code>
</td>
<td>Auto-download and OCR references before main processing.</td>
<td>
  • Multi-source context<br/>
  • External docs analysis<br/>
  • Comprehensive research<br/>
  • Data aggregation
</td>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/🤝-Human--Loop-2ECC71?style=for-the-badge" alt="hitl"/>
  <br/><code>hitl-interactive</code>
</td>
<td>Approval checkpoints at every critical decision point.</td>
<td>
  • High-stakes work<br/>
  • Expert-guided analysis<br/>
  • Full control needed<br/>
  • Compliance workflows
</td>
</tr>

<tr>
<td align="center">
  <img src="https://img.shields.io/badge/💬-Copilot-34495E?style=for-the-badge" alt="copilot"/>
  <br/><code>copilot</code>
</td>
<td>Conversational interface with persistent context and memory.</td>
<td>
  • Exploratory analysis<br/>
  • Iterative problem-solving<br/>
  • Interactive development<br/>
  • Pair programming
</td>
</tr>

</table>

</details>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🏗️ System Architecture

<div align="center">

```
╔══════════════════════════════════════════════════════════════════╗
║                     🎨 FRONTEND LAYER                            ║
║              Next.js 14  •  React 18  •  TypeScript              ║
║         Real-time Socket.IO  •  DAG Visualization                ║
║              TailwindCSS  •  @xyflow/react                       ║
╠══════════════════════════════════════════════════════════════════╣
║                     ⚡ BACKEND LAYER                              ║
║           FastAPI  •  Uvicorn  •  WebSockets                     ║
║       REST API  •  Task Engine  •  Event Streaming               ║
║         SQLAlchemy  •  Alembic  •  Pydantic                      ║
╠══════════════════════════════════════════════════════════════════╣
║                  🤖 AGENT FRAMEWORK CORE                          ║
║             AG2 Multi-Agent Orchestration Engine                 ║
║      50+ Specialized Agents  •  DAG Execution                    ║
║         RAG Pipeline  •  Tool Integration                        ║
╠══════════════════════════════════════════════════════════════════╣
║                   💾 DATA & STORAGE LAYER                         ║
║        SQLAlchemy ORM  •  SQLite / PostgreSQL                    ║
║      File Tracking  •  Cost Records  •  Event Logs               ║
║            Alembic Migrations  •  JSONB Support                  ║
╠══════════════════════════════════════════════════════════════════╣
║                    🔌 INTEGRATION LAYER                           ║
║         CrewAI Tools  •  LangChain Tools                         ║
║      External APIs  •  Web Scraping  •  Document Processing      ║
╚══════════════════════════════════════════════════════════════════╝
```

</div>

<br/>

### 🔧 Technology Stack

<div align="center">

<table>
<tr>
<td valign="top" width="33%">

#### **🎨 Frontend**
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=flat&logo=socket.io&logoColor=white)

- Next.js 14 (App Router)
- React 18 with Hooks
- TypeScript 5
- TailwindCSS 3.3
- Socket.IO Client 4.7
- @xyflow/react (DAG viz)

</td>
<td valign="top" width="33%">

#### **⚡ Backend**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

- Python 3.12+
- FastAPI & Uvicorn
- SQLAlchemy ORM
- Alembic (migrations)
- WebSockets
- Pydantic validation

</td>
<td valign="top" width="33%">

#### **🤖 AI & LLMs**
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-191919?style=flat&logo=anthropic&logoColor=white)
![Google](https://img.shields.io/badge/Gemini-4285F4?style=flat&logo=google&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-121212?style=flat&logo=chainlink&logoColor=white)

- AG2 (AutoGen 2)
- OpenAI GPT-4 / GPT-4o
- Anthropic Claude
- Google Gemini
- Mistral API
- Perplexity API

</td>
</tr>
</table>

</div>

<br/>

### 📊 System Flow

```mermaid
graph TB
    A[User Request] -->|REST/WebSocket| B[FastAPI Backend]
    B --> C{Task Type}
    C -->|Research| D[Research Agents]
    C -->|Code| E[Engineering Agents]
    C -->|Analysis| F[Analysis Agents]
    D --> G[AG2 Orchestrator]
    E --> G
    F --> G
    G --> H[LLM Provider]
    H --> I[Response Processing]
    I --> J[Database Storage]
    I --> K[Real-time Updates]
    K -->|WebSocket| L[Next.js Frontend]
    J --> L
    
    style A fill:#00D9FF
    style G fill:#9B59B6
    style L fill:#2ECC71
```

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🤖 Agent Ecosystem

Asteroid orchestrates **50+ specialized agents** organized by function:

<details>
<summary><h3>🔍 View All Agents</h3></summary>

<br/>

<div align="center">

<table>
<tr>
<td width="25%" valign="top">

#### 🧭 Planning Agents
![Planning](https://img.shields.io/badge/Planning-5-00D9FF?style=flat-square)

| Agent | Role |
|-------|------|
| `planner` | Task breakdown & strategic planning |
| `task_improver` | Description refinement & optimization |
| `plan_recorder` | Plan persistence & versioning |
| `plan_reviewer` | Quality assurance & validation |
| `plan_setter` | Plan activation & deployment |

</td>
<td width="25%" valign="top">

#### ⚙️ Execution Agents
![Execution](https://img.shields.io/badge/Execution-10-3498DB?style=flat-square)

| Agent | Role |
|-------|------|
| `engineer` | Code generation & development |
| `researcher` | Research & data analysis |
| `executor` | Sandboxed code execution |
| `executor_bash` | Shell command execution |
| `installer` | Package management |
| `debugger` | Error diagnosis & fixing |
| `tester` | Test generation & validation |
| `optimizer` | Performance optimization |
| `refactor` | Code refactoring |
| `documenter` | Documentation generation |

</td>
<td width="25%" valign="top">

#### 🔍 Retrieval Agents
![Retrieval](https://img.shields.io/badge/Retrieval-8-9B59B6?style=flat-square)

| Agent | Role |
|-------|------|
| `rag_agents` | RAG pipeline orchestration |
| `retrieve_assistant` | Document retrieval & indexing |
| `web_surfer` | Web browsing & scraping |
| `perplexity` | AI-powered search |
| `arxiv_researcher` | Academic paper discovery |
| `data_collector` | Data aggregation |
| `content_extractor` | Content parsing |
| `summarizer` | Intelligent summarization |

</td>
<td width="25%" valign="top">

#### 🛠️ Utility Agents
![Utility](https://img.shields.io/badge/Utility-12-2ECC71?style=flat-square)

| Agent | Role |
|-------|------|
| `idea_maker` | Creative ideation |
| `idea_hater` | Critical review & validation |
| `validator` | Output validation |
| `formatter` | Content formatting |
| `translator` | Language translation |
| `analyzer` | Data analysis |
| `visualizer` | Data visualization |
| `reporter` | Report generation |
| `coordinator` | Multi-agent coordination |
| `terminator` | Task completion |
| `copilot_control` | Copilot orchestration |
| `quality_checker` | Quality assurance |

</td>
</tr>
</table>

</div>

</details>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🚀 Quick Start

### 📋 Prerequisites

<div align="center">

| Requirement | Version | Status |
|:------------|:--------|:-------|
| 🐍 **Python** | >= 3.12 | ![Required](https://img.shields.io/badge/Required-FF6B6B?style=flat-square) |
| 📦 **Node.js** | >= 18 | ![Required](https://img.shields.io/badge/Required-FF6B6B?style=flat-square) |
| 🔧 **npm** | >= 9 | ![Required](https://img.shields.io/badge/Required-FF6B6B?style=flat-square) |
| 🔑 **API Keys** | LLM Provider | ![Required](https://img.shields.io/badge/Required-FF6B6B?style=flat-square) |
| 🐳 **Docker** | Latest | ![Optional](https://img.shields.io/badge/Optional-4ECDC4?style=flat-square) |

</div>

<br/>

### 📥 Installation

<details open>
<summary><h4>🔧 Standard Installation</h4></summary>

```bash
# 1️⃣ Clone the repository
git clone https://github.com/keshav/Asteroid.git
cd Asteroid

# 2️⃣ Backend Setup
python -m venv .venv

# On Windows
.venv\Scripts\activate

# On macOS/Linux
source .venv/bin/activate

# Install dependencies
pip install -e .

# 3️⃣ Optional: Install data science tools
pip install -e ".[data]"       # scipy, matplotlib, xgboost

# 4️⃣ Optional: Install Jupyter support
pip install -e ".[jupyter]"

# 5️⃣ Frontend Setup
cd Asteroid-ui
npm install
cd ..
```

</details>

<details>
<summary><h4>🐳 Docker Installation</h4></summary>

```bash
# Clone the repository
git clone https://github.com/keshav/Asteroid.git
cd Asteroid

# Build and run with Docker Compose
docker-compose up --build

# Or build Docker image manually
docker build -t Asteroid .
docker run -p 3000:3000 -p 8000:8000 \
  -e OPENAI_API_KEY=your-key \
  Asteroid
```

</details>

<br/>

### ⚙️ Configuration

<details open>
<summary><h4>🔐 Environment Setup</h4></summary>

**Create `.env` file in project root:**

```bash
# Required: At least one LLM provider
OPENAI_API_KEY=sk-...

# Optional: Additional providers
ANTHROPIC_API_KEY=sk-ant-...
GEMINI_API_KEY=...
PERPLEXITY_API_KEY=pplx-...
MISTRAL_API_KEY=...

# Optional: Azure OpenAI
AZURE_OPENAI_API_KEY=...
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_DEPLOYMENT=gpt-4o
AZURE_OPENAI_API_VERSION=2024-12-01-preview

# Work Directory (default: ~/Desktop/cmbdir)
CMBAGENT_DEFAULT_WORK_DIR=~/Desktop/cmbdir

# Database (optional - defaults to SQLite)
DATABASE_URL=postgresql://user:pass@localhost/Asteroid

# Logging
LOG_LEVEL=INFO
LOG_JSON=false
```

**Create `Asteroid-ui/.env.local` for frontend:**

```bash
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_CMBAGENT_WORK_DIR=~/Desktop/cmbdir
```

</details>

<br/>

### 🎯 Running Asteroid

<details open>
<summary><h4>💻 Development Mode</h4></summary>

```bash
# Terminal 1: Start Backend
cd backend
python run.py
# → Backend API: http://localhost:8000
# → API Docs: http://localhost:8000/docs

# Terminal 2: Start Frontend
cd Asteroid-ui
npm run dev
# → Web UI: http://localhost:3000
```

</details>

<details>
<summary><h4>🐳 Docker Mode</h4></summary>

```bash
# Using Docker Compose (recommended)
docker-compose up --build

# Access the application:
# → Web UI: http://localhost:3000
# → Backend API: http://localhost:8000
# → API Docs: http://localhost:8000/docs
```

</details>

<br/>

### ✅ Verify Installation

<div align="center">

```mermaid
graph LR
    A[Open Browser] --> B[http://localhost:3000]
    B --> C{Asteroid UI Loads?}
    C -->|✅ Yes| D[Check Backend]
    C -->|❌ No| E[Check Logs]
    D --> F[http://localhost:8000/health]
    F --> G{Status: OK?}
    G -->|✅ Yes| H[🎉 Success!]
    G -->|❌ No| E
    
    style H fill:#2ECC71
    style E fill:#E74C3C
```

**Verification Checklist:**

✅ Web UI accessible at `http://localhost:3000`  
✅ Backend health check at `http://localhost:8000/health`  
✅ API documentation at `http://localhost:8000/docs`  
✅ WebSocket connection established  
✅ Database initialized

</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 📡 API Reference

<div align="center">

**🔗 Full interactive API documentation available at:**  
**[http://localhost:8000/docs](http://localhost:8000/docs)**

</div>

<br/>

### 🎯 Core Endpoints

<details open>
<summary><h4>📋 Task Management</h4></summary>

| Method | Endpoint | Description |
|:-------|:---------|:------------|
| `POST` | `/tasks` | Create a new task with mode and configuration |
| `GET` | `/tasks/{id}` | Retrieve task status and details |
| `POST` | `/tasks/{id}/execute` | Execute a configured task |
| `DELETE` | `/tasks/{id}` | Delete a task |
| `GET` | `/tasks` | List all tasks with filtering |

</details>

<details>
<summary><h4>🔄 Runs & Execution</h4></summary>

| Method | Endpoint | Description |
|:-------|:---------|:------------|
| `POST` | `/runs` | Start a new task run |
| `GET` | `/runs/{id}` | Get run details and results |
| `GET` | `/runs/{id}/output` | Stream run output in real-time |
| `POST` | `/runs/{id}/cancel` | Cancel a running task |
| `GET` | `/runs/{id}/logs` | Retrieve execution logs |

</details>

<details>
<summary><h4>💬 Sessions & Copilot</h4></summary>

| Method | Endpoint | Description |
|:-------|:---------|:------------|
| `POST` | `/sessions` | Create a new copilot session |
| `POST` | `/sessions/{id}/message` | Send message to copilot |
| `GET` | `/sessions/{id}` | Get session history |
| `DELETE` | `/sessions/{id}` | End a session |

</details>

<details>
<summary><h4>🔬 Deep Research</h4></summary>

| Method | Endpoint | Description |
|:-------|:---------|:------------|
| `POST` | `/api/deepresearch/create` | Create deep research task |
| `POST` | `/api/deepresearch/{id}/stages/{num}/execute` | Execute research stage |
| `GET` | `/api/deepresearch/{id}` | Get research status |

</details>

<details>
<summary><h4>🔌 WebSocket Events</h4></summary>

**Connection:** `ws://localhost:8000/ws/{task_id}`

```typescript
// Event types received via WebSocket
interface WebSocketEvents {
  status: {
    task_id: string;
    status: "pending" | "running" | "completed" | "failed";
  };
  
  output: {
    content: string;
    timestamp: number;
  };
  
  dag_update: {
    nodes: Node[];
    edges: Edge[];
  };
  
  approval_request: {
    message: string;
    options: string[];
  };
  
  cost_update: {
    tokens: number;
    cost: number;
  };
  
  file_created: {
    path: string;
    size: number;
  };
  
  error: {
    message: string;
    code: string;
  };
}
```

</details>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🎓 Use Cases & Examples

<div align="center">

### 🌐 Real-World Applications

</div>

<br/>

<table>
<tr>
<td width="50%" valign="top">

### 📊 **Research & Analysis**

<details>
<summary><strong>🔍 Market Research</strong></summary>

```python
from cmbagent import CMBAgent

agent = CMBAgent(mode="planning-control")
result = agent.run("""
  Analyze the current state of AI-powered 
  code generation tools:
  - Market size and growth
  - Key players and offerings
  - Competitive advantages
  - Future trends
""")
```
</details>

<details>
<summary><strong>📚 Literature Review</strong></summary>

```python
agent = CMBAgent(mode="arxiv")
result = agent.run("""
  Survey recent papers on transformer 
  architectures for computer vision
  from 2024, summarize key findings
""")
```
</details>

<details>
<summary><strong>🔬 Product Discovery</strong></summary>

```python
agent = CMBAgent(mode="idea-generation")
result = agent.run("""
  Generate innovative features for a 
  developer productivity tool targeting
  remote teams
""")
```
</details>

</td>
<td width="50%" valign="top">

### 📝 **Content & Documentation**

<details>
<summary><strong>📄 Research Papers</strong></summary>

```python
agent = CMBAgent(mode="deep-research")
result = agent.run("""
  Write a complete research paper on
  'Multi-Agent Systems for Scientific
  Discovery' with methodology, 
  experiments, and LaTeX formatting
""")
```
</details>

<details>
<summary><strong>📰 Weekly Reports</strong></summary>

```python
agent = CMBAgent(mode="hitl-interactive")
result = agent.run("""
  Create a weekly AI technology report
  covering major developments, with
  human approval at each section
""")
```
</details>

<details>
<summary><strong>📝 Release Notes</strong></summary>

```python
agent = CMBAgent(mode="one-shot")
result = agent.run("""
  Generate release notes from Git history
  for version 2.0, categorized by feature,
  bugfix, and breaking changes
""")
```
</details>

</td>
</tr>
</table>

<br/>

<div align="center">

### 💼 Enterprise Workflows

</div>

<br/>

<table>
<tr>
<td width="33%" valign="top" align="center">

<img src="https://img.shields.io/badge/Code%20Review-Automated-00D9FF?style=for-the-badge" alt="Code Review"/>

**Multi-Dimensional Analysis**
- Correctness verification
- Security audit
- Performance optimization
- Style compliance

</td>
<td width="33%" valign="top" align="center">

<img src="https://img.shields.io/badge/RFP%20Response-Intelligent-9B59B6?style=for-the-badge" alt="RFP"/>

**Proposal Generation**
- Context gathering
- Requirement analysis
- Solution design
- Document compilation

</td>
<td width="33%" valign="top" align="center">

<img src="https://img.shields.io/badge/Competitive%20Intel-Strategic-2ECC71?style=for-the-badge" alt="Intel"/>

**Market Intelligence**
- Competitor tracking
- Feature comparison
- Market positioning
- Trend analysis

</td>
</tr>
</table>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🧪 Testing

```bash
# Run all tests
pytest

# Run with coverage report
pytest --cov=cmbagent --cov-report=html --cov-report=term

# Skip slow tests
pytest -m "not slow"

# Integration tests only
pytest -m integration

# Verbose output with detailed logging
pytest -v --log-cli-level=DEBUG

# Run specific test file
pytest tests/test_agents.py

# Run tests in parallel (faster)
pytest -n auto
```

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 📚 Documentation

<div align="center">

| Resource | Link | Description |
|:---------|:-----|:------------|
| 📖 **Full Documentation** | [Coming Soon] | Complete user guide and tutorials |
| 🔧 **API Reference** | [localhost:8000/docs](http://localhost:8000/docs) | Interactive API documentation |
| 💡 **Examples** | [`/examples`](./examples) | Code samples and use cases |
| 🏗️ **Architecture** | [`/docs`](./docs) | System design and architecture |
| 🎯 **Task Guides** | [`/docs`](./docs) | Task-specific documentation |

</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🤝 Contributing

<div align="center">

**Contributions are welcome!** 🎉

</div>

<br/>

### 🔧 How to Contribute

```mermaid
graph LR
    A[🍴 Fork Repo] --> B[🔀 Create Branch]
    B --> C[💻 Make Changes]
    C --> D[✅ Run Tests]
    D --> E[📝 Commit]
    E --> F[🚀 Push]
    F --> G[🔁 Pull Request]
    
    style A fill:#00D9FF
    style G fill:#2ECC71
```

<br/>

```bash
# 1️⃣ Fork the repository on GitHub

# 2️⃣ Clone your fork
git clone https://github.com/your-username/Asteroid.git
cd Asteroid

# 3️⃣ Create a feature branch
git checkout -b feature/AmazingFeature

# 4️⃣ Make your changes and commit
git add .
git commit -m 'Add some AmazingFeature'

# 5️⃣ Push to your fork
git push origin feature/AmazingFeature

# 6️⃣ Open a Pull Request on GitHub
```

<br/>

### 📝 Contribution Guidelines

- ✅ Write clear, descriptive commit messages
- ✅ Add tests for new features
- ✅ Update documentation as needed
- ✅ Follow existing code style
- ✅ Ensure all tests pass before submitting

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 📄 License

<div align="center">

This project is licensed under the **Apache License 2.0**

See the [LICENSE](LICENSE) file for details

**Free for commercial and personal use** ✨

</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 🙏 Acknowledgments

<div align="center">

<table>
<tr>
<td align="center" width="25%">
  <img src="https://img.shields.io/badge/AG2-AutoGen%202-00D9FF?style=for-the-badge&logo=openai" alt="AG2"/><br/>
  <strong>AG2 Framework</strong><br/>
  <sub>Multi-agent foundation</sub>
</td>
<td align="center" width="25%">
  <img src="https://img.shields.io/badge/CrewAI-Tools-9B59B6?style=for-the-badge&logo=robot" alt="CrewAI"/><br/>
  <strong>CrewAI</strong><br/>
  <sub>Tool integration</sub>
</td>
<td align="center" width="25%">
  <img src="https://img.shields.io/badge/LangChain-Chain-2ECC71?style=for-the-badge&logo=chainlink" alt="LangChain"/><br/>
  <strong>LangChain</strong><br/>
  <sub>LLM orchestration</sub>
</td>
<td align="center" width="25%">
  <img src="https://img.shields.io/badge/shadcn%2Fui-Components-000000?style=for-the-badge&logo=shadcnui" alt="shadcn"/><br/>
  <strong>shadcn/ui</strong><br/>
  <sub>UI components</sub>
</td>
</tr>
</table>

</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

<br/>

## 📬 Contact & Support

<div align="center">

<h3>👨‍💻 Maintained by Keshav</h3>

<br/>

<table>
<tr>
<td align="center">
  <a href="https://github.com/keshav">
    <img src="https://img.shields.io/badge/GitHub-keshav-181717?style=for-the-badge&logo=github" alt="GitHub"/>
  </a>
</td>
<td align="center">
  <a href="mailto:keshav@example.com">
    <img src="https://img.shields.io/badge/Email-keshav@example.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</td>
<td align="center">
  <a href="https://github.com/keshav/Asteroid/issues">
    <img src="https://img.shields.io/badge/Issues-Report%20Bug-FF6B6B?style=for-the-badge&logo=github" alt="Issues"/>
  </a>
</td>
<td align="center">
  <a href="https://github.com/keshav/Asteroid/discussions">
    <img src="https://img.shields.io/badge/Discussions-Q%26A-4ECDC4?style=for-the-badge&logo=github" alt="Discussions"/>
  </a>
</td>
</tr>
</table>

<br/>

### 📝 Project Information

**Repository:** [github.com/keshav/Asteroid](https://github.com/keshav/Asteroid)  
**Documentation:** [Coming Soon]  
**Logs Location:** `~/.cmbagent/logs/backend.log`

<br/>

### 💬 Get Help

<table>
<tr>
<td width="50%" align="center">
  <h4>🐛 Found a Bug?</h4>
  <a href="https://github.com/keshav/Asteroid/issues/new?template=bug_report.md">
    <img src="https://img.shields.io/badge/Report-Bug-FF6B6B?style=for-the-badge" alt="Report Bug"/>
  </a>
</td>
<td width="50%" align="center">
  <h4>💡 Have an Idea?</h4>
  <a href="https://github.com/keshav/Asteroid/issues/new?template=feature_request.md">
    <img src="https://img.shields.io/badge/Request-Feature-4ECDC4?style=for-the-badge" alt="Feature Request"/>
  </a>
</td>
</tr>
</table>

<br/>

---

<br/>

<h3>⭐ Star this repo if you find it useful!</h3>

<br/>

<img src="https://img.shields.io/github/stars/keshav/Asteroid?style=social" alt="GitHub stars"/>

<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=150&section=footer&text=Asteroid&fontSize=50&fontAlignY=70&desc=Multi-Agent%20Research%20System&descSize=20&descAlignY=90&animation=twinkling" alt="Footer"/>

</div>

<br/>

<div align="center">

**Made with ❤️ by Keshav**

*Transforming complex workflows into intelligent automation*

</div>



