# 📝 Changelog

All notable changes to the MARS project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

<div align="center">

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" alt="divider"/>

</div>

## [Unreleased]

### 🎉 Initial Release - 2024-01-15

#### ✨ Added
- Initial public release of MARS (Multi-Agent Research System)
- 8 execution modes for different workflow patterns
- 50+ specialized AI agents organized by function
- FastAPI backend with full REST API
- Next.js 14 frontend with real-time WebSocket updates
- AG2 (AutoGen 2) multi-agent orchestration
- Support for multiple LLM providers (OpenAI, Anthropic, Gemini, Mistral)
- RAG pipeline for knowledge retrieval
- Human-in-the-loop approval system
- Real-time DAG visualization
- Cost tracking and monitoring
- SQLAlchemy ORM with SQLite/PostgreSQL support
- Docker deployment support
- Comprehensive documentation and examples

#### 🔧 Execution Modes
- `one-shot`: Single-pass direct execution
- `planning-control`: Multi-step research with planning
- `idea-generation`: Adversarial ideation loop
- `ocr`: Document extraction with Mistral OCR
- `arxiv`: Literature review and paper analysis
- `enhance-input`: Input enrichment with auto-download
- `hitl-interactive`: Human-in-the-loop with approval checkpoints
- `copilot`: Conversational interface with persistent context

#### 🤖 Agent Categories
- **Planning Agents**: Task breakdown and strategic planning (5 agents)
- **Execution Agents**: Code generation and development (10 agents)
- **Retrieval Agents**: Research and data gathering (8 agents)
- **Utility Agents**: Supporting functions and validation (12+ agents)

#### 🔌 Integrations
- CrewAI tools integration
- LangChain tools support
- ArXiv API for academic papers
- DuckDuckGo search
- Web scraping capabilities
- Perplexity AI search

#### 📚 Documentation
- Comprehensive README with architecture diagrams
- CONTRIBUTING.md with development guidelines
- CODE_OF_CONDUCT.md for community standards
- ARCHITECTURE.md with technical deep-dive
- API documentation via FastAPI Swagger UI
- Example scripts and use cases

#### 🧪 Testing
- Pytest test suite
- Integration tests
- Unit tests for core functionality
- Test coverage reporting

#### 🐳 Deployment
- Docker and Docker Compose support
- Multi-stage Docker builds
- Environment configuration templates
- Production-ready setup examples

---

<div align="center">

## 📋 Version History

| Version | Date | Highlights |
|:--------|:-----|:-----------|
| 0.0.1 | 2024-01-15 | Initial public release |

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

## 🔮 Upcoming Features

- [ ] Enhanced visualization with interactive DAG
- [ ] Plugin system for custom agents
- [ ] Multi-user support with authentication
- [ ] Advanced cost optimization strategies
- [ ] Integration with more LLM providers
- [ ] Mobile-responsive UI improvements
- [ ] Agent marketplace for sharing custom agents
- [ ] Advanced caching mechanisms
- [ ] Performance monitoring dashboard
- [ ] Automated testing pipeline

<br/>

---

**Maintained by Keshav**

For detailed information about each release, see the [GitHub Releases](https://github.com/keshav/mars/releases) page.

</div>
