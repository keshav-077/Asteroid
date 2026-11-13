# 🤝 Contributing to MARS

<div align="center">

**Thank you for your interest in contributing to MARS!** 🎉

We welcome contributions from the community and are grateful for your support.

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" alt="divider"/>

</div>

## 📋 Table of Contents

- [Code of Conduct](#-code-of-conduct)
- [Getting Started](#-getting-started)
- [Development Setup](#-development-setup)
- [How to Contribute](#-how-to-contribute)
- [Pull Request Process](#-pull-request-process)
- [Style Guidelines](#-style-guidelines)
- [Testing Guidelines](#-testing-guidelines)
- [Community](#-community)

## 📜 Code of Conduct

This project adheres to a Code of Conduct that all contributors are expected to follow. Please read [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) before contributing.

## 🚀 Getting Started

### Prerequisites

- Python 3.12 or higher
- Node.js 18 or higher
- Git
- Basic understanding of multi-agent systems
- Familiarity with FastAPI and React

### Areas of Contribution

We welcome contributions in the following areas:

- 🐛 **Bug Fixes**: Help us identify and fix bugs
- ✨ **New Features**: Propose and implement new features
- 📝 **Documentation**: Improve or translate documentation
- 🎨 **UI/UX**: Enhance the user interface and experience
- 🧪 **Tests**: Write tests to improve code coverage
- 🔧 **Tools**: Create new tools and integrations
- 🤖 **Agents**: Develop new specialized agents
- 📊 **Examples**: Add examples and tutorials

## 💻 Development Setup

### 1. Fork and Clone

```bash
# Fork the repository on GitHub
# Then clone your fork
git clone https://github.com/YOUR_USERNAME/mars.git
cd mars

# Add upstream remote
git remote add upstream https://github.com/keshav/mars.git
```

### 2. Set Up Backend

```bash
# Create virtual environment
python -m venv .venv

# Activate virtual environment
# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate

# Install in development mode with all dependencies
pip install -e ".[data,jupyter]"

# Install development dependencies
pip install pytest pytest-cov black flake8 mypy pre-commit
```

### 3. Set Up Frontend

```bash
cd mars-ui
npm install
npm run dev
cd ..
```

### 4. Configure Environment

```bash
# Copy example environment file
cp .env.example .env

# Add your API keys to .env
# At minimum, add OPENAI_API_KEY or ANTHROPIC_API_KEY
```

### 5. Set Up Pre-commit Hooks (Recommended)

```bash
# Install pre-commit hooks
pre-commit install

# Run hooks manually
pre-commit run --all-files
```

## 🎯 How to Contribute

### Reporting Bugs

1. **Check existing issues** to avoid duplicates
2. **Use the bug report template** when creating a new issue
3. **Include detailed information**:
   - Steps to reproduce
   - Expected vs actual behavior
   - System information (OS, Python version, etc.)
   - Error messages and logs
   - Screenshots if applicable

### Suggesting Features

1. **Check existing feature requests** to avoid duplicates
2. **Use the feature request template**
3. **Provide context**:
   - Clear description of the feature
   - Use cases and benefits
   - Potential implementation approach
   - Any alternatives considered

### Improving Documentation

- Fix typos, grammar, or clarify existing docs
- Add missing documentation
- Create tutorials and guides
- Translate documentation to other languages
- Update outdated information

### Code Contributions

1. **Pick an issue** or create one for discussion
2. **Comment on the issue** to let others know you're working on it
3. **Create a feature branch** from `main`
4. **Make your changes** following our style guidelines
5. **Write tests** for new functionality
6. **Update documentation** as needed
7. **Submit a pull request**

## 🔄 Pull Request Process

### Before Submitting

- [ ] Code follows style guidelines
- [ ] All tests pass (`pytest`)
- [ ] New tests added for new features
- [ ] Documentation updated
- [ ] Commit messages are clear and descriptive
- [ ] No merge conflicts with `main`

### Creating a Pull Request

1. **Create a feature branch**

```bash
git checkout -b feature/amazing-feature
# or
git checkout -b fix/bug-description
```

2. **Make your changes and commit**

```bash
git add .
git commit -m "feat: add amazing feature"
# or
git commit -m "fix: resolve bug with agent coordination"
```

3. **Push to your fork**

```bash
git push origin feature/amazing-feature
```

4. **Open a Pull Request** on GitHub

### Pull Request Title Format

Follow [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code style changes (formatting, etc.)
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks
- `perf:` Performance improvements

**Examples:**
- `feat: add adversarial validation mode`
- `fix: resolve WebSocket connection timeout`
- `docs: update installation guide for Windows`

### Pull Request Description

Include:

- **Summary** of changes
- **Motivation** for the changes
- **Testing** performed
- **Screenshots** (for UI changes)
- **Breaking changes** (if any)
- **Related issues** (e.g., "Fixes #123")

### Review Process

1. Maintainers will review your PR
2. Address any requested changes
3. Once approved, a maintainer will merge your PR
4. Your contribution will be included in the next release! 🎉

## 🎨 Style Guidelines

### Python Code Style

We follow [PEP 8](https://pep8.org/) with some modifications:

```bash
# Format code with Black
black cmbagent/ backend/ tests/

# Check with flake8
flake8 cmbagent/ backend/ tests/

# Type checking with mypy
mypy cmbagent/
```

#### Key Points

- **Line length**: 100 characters (Black default)
- **Imports**: Use absolute imports, group them (stdlib, third-party, local)
- **Type hints**: Use type hints for function signatures
- **Docstrings**: Use Google-style docstrings

**Example:**

```python
from typing import List, Optional

from pydantic import BaseModel

from cmbagent.base_agent import BaseAgent


class TaskConfig(BaseModel):
    """Configuration for a task execution.
    
    Args:
        task_id: Unique identifier for the task
        mode: Execution mode (one-shot, planning-control, etc.)
        max_rounds: Maximum number of agent interaction rounds
    """
    
    task_id: str
    mode: str
    max_rounds: int = 10
    
    def validate(self) -> bool:
        """Validate the task configuration.
        
        Returns:
            True if configuration is valid
            
        Raises:
            ValueError: If configuration is invalid
        """
        if self.max_rounds < 1:
            raise ValueError("max_rounds must be at least 1")
        return True
```

### TypeScript/JavaScript Style

- Use **TypeScript** for type safety
- Follow **ESLint** configuration
- Use **Prettier** for formatting
- Use **functional components** with hooks

```bash
# Format code
cd mars-ui
npm run lint
npm run format
```

### Git Commit Messages

- Use imperative mood ("add feature" not "added feature")
- Keep first line under 72 characters
- Reference issues and PRs

```
feat: add real-time agent monitoring

- Implement WebSocket connection for live updates
- Add DAG visualization component
- Update backend to emit agent events

Closes #123
```

## 🧪 Testing Guidelines

### Running Tests

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=cmbagent --cov-report=html

# Run specific test file
pytest tests/test_agents.py

# Run tests in parallel
pytest -n auto
```

### Writing Tests

- Write tests for all new features
- Maintain or improve code coverage
- Use descriptive test names
- Include both unit and integration tests

**Example:**

```python
import pytest
from cmbagent.base_agent import BaseAgent


class TestBaseAgent:
    """Tests for BaseAgent class."""
    
    def test_agent_initialization(self):
        """Test that agent initializes with correct configuration."""
        agent = BaseAgent(name="test_agent", role="tester")
        assert agent.name == "test_agent"
        assert agent.role == "tester"
    
    def test_agent_execution(self):
        """Test that agent can execute a simple task."""
        agent = BaseAgent(name="test_agent")
        result = agent.execute("Hello, world!")
        assert result is not None
        assert isinstance(result, str)
    
    @pytest.mark.integration
    def test_agent_with_llm(self, openai_client):
        """Integration test with actual LLM."""
        agent = BaseAgent(name="test_agent", client=openai_client)
        result = agent.execute("What is 2+2?")
        assert "4" in result
```

## 👥 Community

### Communication Channels

- **GitHub Issues**: Bug reports and feature requests
- **GitHub Discussions**: Questions and general discussion
- **Pull Requests**: Code reviews and contributions

### Getting Help

If you need help:

1. Check the [documentation](README.md)
2. Search [existing issues](https://github.com/keshav/mars/issues)
3. Ask in [GitHub Discussions](https://github.com/keshav/mars/discussions)
4. Create a new issue with the "question" label

### Recognition

Contributors will be recognized in:

- Release notes
- GitHub contributors list
- Special mentions for significant contributions

## 📄 License

By contributing to MARS, you agree that your contributions will be licensed under the Apache License 2.0.

---

<div align="center">

**Thank you for contributing to MARS!** ❤️

**Made with 💙 by the MARS Community**

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" alt="divider"/>

</div>
