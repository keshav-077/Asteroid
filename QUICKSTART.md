# ⚡ MARS Quick Start Guide

<div align="center">

**Get up and running with MARS in under 10 minutes!**

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" alt="divider"/>

</div>

## 🎯 What You'll Achieve

By the end of this guide, you'll:
- ✅ Have MARS installed and running locally
- ✅ Execute your first multi-agent task
- ✅ Understand the basic execution modes
- ✅ Know how to configure different LLM providers

<br/>

## 📋 Prerequisites Checklist

Before starting, ensure you have:

- [ ] Python 3.12 or higher installed
- [ ] Node.js 18 or higher installed
- [ ] npm 9 or higher installed
- [ ] At least one LLM API key (OpenAI, Anthropic, Gemini, etc.)
- [ ] Git installed

**Check your versions:**
```bash
python --version    # Should be 3.12+
node --version      # Should be 18+
npm --version       # Should be 9+
```

<br/>

## 🚀 Installation (5 minutes)

### Step 1: Clone and Navigate

```bash
# Clone the repository
git clone https://github.com/keshav/mars.git
cd mars
```

### Step 2: Backend Setup

```bash
# Create virtual environment
python -m venv .venv

# Activate it (choose your OS)
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

# Install MARS
pip install -e .
```

### Step 3: Frontend Setup

```bash
# Navigate to frontend and install
cd mars-ui
npm install
cd ..
```

### Step 4: Configure Environment

```bash
# Copy example environment file
cp .env.example .env

# Edit .env and add your API key
# On Windows: notepad .env
# On macOS/Linux: nano .env
```

**Add at minimum:**
```bash
OPENAI_API_KEY=sk-your-key-here
# OR
ANTHROPIC_API_KEY=sk-ant-your-key-here
# OR
GEMINI_API_KEY=your-gemini-key-here
```

<br/>

## 🎮 Running MARS (2 minutes)

### Option A: Development Mode (Recommended for First-Time)

**Terminal 1 - Backend:**
```bash
cd backend
python run.py
```

You should see:
```
INFO:     Started server process
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://127.0.0.1:8000
```

**Terminal 2 - Frontend:**
```bash
cd mars-ui
npm run dev
```

You should see:
```
✓ Ready in 2.3s
○ Local:   http://localhost:3000
```

### Option B: Docker (One Command)

```bash
docker-compose up --build
```

<br/>

## ✅ Verify Installation (1 minute)

Open your browser and check these URLs:

1. **Frontend**: http://localhost:3000
   - You should see the MARS dashboard

2. **Backend Health**: http://localhost:8000/health
   - You should see: `{"status":"healthy"}`

3. **API Docs**: http://localhost:8000/docs
   - You should see interactive API documentation

<br/>

## 🎯 Your First Task (2 minutes)

### Using the Web UI

1. Open http://localhost:3000
2. Click **"New Task"**
3. Enter:
   - **Name**: My First Analysis
   - **Mode**: one-shot
   - **Task Description**: "Analyze the benefits of using multi-agent systems in AI research"
4. Click **"Execute"**
5. Watch the agents work in real-time!

### Using the API

```bash
# Create a task via curl
curl -X POST http://localhost:8000/tasks \
  -H "Content-Type: application/json" \
  -d '{
    "name": "My First Analysis",
    "mode": "one-shot",
    "description": "Analyze the benefits of using multi-agent systems in AI research",
    "config": {
      "max_rounds": 10
    }
  }'
```

### Using Python SDK

```python
from cmbagent import CMBAgent

# Initialize agent
agent = CMBAgent(mode="one-shot")

# Run a simple analysis
result = agent.run("""
Analyze the benefits of using multi-agent systems 
in AI research. Provide a structured summary.
""")

print(result)
```

<br/>

## 🎨 Trying Different Modes

### One-Shot Mode (Quick Tasks)
```python
agent = CMBAgent(mode="one-shot")
result = agent.run("Generate a Python function to calculate Fibonacci numbers")
```

### Planning-Control Mode (Complex Research)
```python
agent = CMBAgent(mode="planning-control")
result = agent.run("""
Research the current state of quantum computing:
- Market leaders
- Recent breakthroughs
- Commercial applications
""")
```

### Idea Generation Mode (Brainstorming)
```python
agent = CMBAgent(mode="idea-generation")
result = agent.run("""
Generate innovative ideas for improving 
remote team collaboration
""")
```

### Copilot Mode (Interactive)
```python
from cmbagent import CopilotSession

session = CopilotSession()

# Have a conversation
response1 = session.send("What is multi-agent orchestration?")
print(response1)

response2 = session.send("Give me a practical example")
print(response2)
```

<br/>

## 🔧 Common Issues & Solutions

### Issue: "Module 'cmbagent' not found"

**Solution:**
```bash
# Make sure you're in the project root and virtual env is active
pip install -e .
```

### Issue: "Port 8000 already in use"

**Solution:**
```bash
# Find and kill the process using port 8000
# Windows:
netstat -ano | findstr :8000
taskkill /PID <PID> /F

# macOS/Linux:
lsof -ti:8000 | xargs kill -9
```

### Issue: "API key not configured"

**Solution:**
```bash
# Check your .env file exists and has API key
cat .env | grep API_KEY
# Should show: OPENAI_API_KEY=sk-...
```

### Issue: Frontend can't connect to backend

**Solution:**
```bash
# Check mars-ui/.env.local exists with:
echo "NEXT_PUBLIC_API_URL=http://localhost:8000" > mars-ui/.env.local
```

<br/>

## 📚 Next Steps

Now that you're up and running:

1. **Explore Examples**: Check the `/examples` directory
2. **Read Documentation**: See the full [README](README.md)
3. **Try Different Modes**: Experiment with all 8 execution modes
4. **Build Custom Tasks**: Create your own task configurations
5. **Join the Community**: Contribute or ask questions on GitHub

<br/>

## 🎓 Learning Resources

| Resource | Description | Link |
|:---------|:------------|:-----|
| 📖 **Full Documentation** | Complete guide and API reference | [README.md](README.md) |
| 🏗️ **Architecture** | System design and internals | [ARCHITECTURE.md](ARCHITECTURE.md) |
| 🤝 **Contributing** | How to contribute to MARS | [CONTRIBUTING.md](CONTRIBUTING.md) |
| 💡 **Examples** | Code samples and use cases | [/examples](./examples) |
| 🔧 **API Docs** | Interactive API documentation | http://localhost:8000/docs |

<br/>

## 💬 Getting Help

- 🐛 **Found a bug?** [Report it](https://github.com/keshav/mars/issues/new?template=bug_report.md)
- 💡 **Have an idea?** [Request a feature](https://github.com/keshav/mars/issues/new?template=feature_request.md)
- 🤔 **Need help?** [Ask in Discussions](https://github.com/keshav/mars/discussions)

<br/>

---

<div align="center">

## 🎉 You're All Set!

**Start building amazing multi-agent workflows with MARS!**

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

**Made with ❤️ by Keshav**

</div>
