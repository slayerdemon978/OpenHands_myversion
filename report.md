# OpenHands: Complete Technical Guide for Beginners

## Table of Contents
1. [Project Overview](#project-overview)
2. [Core Concepts](#core-concepts)
3. [Architecture Overview](#architecture-overview)
4. [Repository Structure](#repository-structure)
5. [Technical Stack](#technical-stack)
6. [Key Components Deep Dive](#key-components-deep-dive)
7. [Development Workflow](#development-workflow)
8. [Agent System](#agent-system)
9. [Runtime Environments](#runtime-environments)
10. [Frontend Application](#frontend-application)
11. [Evaluation Framework](#evaluation-framework)
12. [Microagents System](#microagents-system)
13. [Configuration and Setup](#configuration-and-setup)
14. [Testing Strategy](#testing-strategy)
15. [Deployment Options](#deployment-options)
16. [Contributing Guidelines](#contributing-guidelines)

---

## Project Overview

### What is OpenHands?

OpenHands (formerly OpenDevin) is an **AI-powered software development platform** that enables autonomous software development through intelligent agents. Think of it as an AI assistant that can:

- **Write and modify code** in any programming language
- **Execute commands** in a terminal environment
- **Browse the web** to gather information
- **Interact with APIs** and external services
- **Manage files and directories**
- **Run tests and debug issues**
- **Create pull requests** and manage version control

### Key Features

1. **Autonomous Development**: AI agents can complete entire software development tasks independently
2. **Multi-Modal Interaction**: Supports text, code, web browsing, and file operations
3. **Extensible Architecture**: Plugin-based system for adding new capabilities
4. **Multiple Runtime Environments**: Docker, cloud-based, and local execution options
5. **Web-Based Interface**: Modern React frontend for easy interaction
6. **Evaluation Framework**: Comprehensive testing against industry benchmarks
7. **Microagents**: Specialized knowledge modules for domain-specific tasks

### Target Users

- **Software Developers**: Automate repetitive coding tasks and get AI assistance
- **DevOps Engineers**: Automate deployment and infrastructure management
- **Researchers**: Study AI agent capabilities and contribute to the field
- **Students**: Learn about AI-powered development tools

---

## Core Concepts

### 1. Agents
**Agents** are the core AI entities that perform software development tasks. They:
- Receive instructions from users
- Plan and execute sequences of actions
- Learn from feedback and observations
- Can delegate tasks to other specialized agents

### 2. Actions and Observations
- **Actions**: Things the agent can do (run commands, edit files, browse web)
- **Observations**: Feedback from the environment (command output, file contents, web page data)

### 3. Runtime Environment
The **Runtime** is where agents execute their actions:
- Sandboxed environment for security
- Supports multiple backends (Docker, cloud services)
- Provides tools and utilities for development tasks

### 4. Event Stream
A central communication hub where:
- All actions and observations are logged
- Components can publish and subscribe to events
- Enables real-time updates and coordination

### 5. State Management
The **State** represents the current context:
- Conversation history
- Active tasks and subtasks
- Agent memory and context
- Execution status

---

## Architecture Overview

OpenHands follows a **modular, event-driven architecture**:

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   Runtime       │
│   (React)       │◄──►│   (FastAPI)     │◄──►│   (Docker/E2B)  │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         │              ┌─────────────────┐              │
         └─────────────►│  Event Stream   │◄─────────────┘
                        └─────────────────┘
                                 │
                        ┌─────────────────┐
                        │   Agent Hub     │
                        │  (AI Agents)    │
                        └─────────────────┘
```

### Data Flow

1. **User Input** → Frontend → Backend → Agent
2. **Agent Planning** → Actions → Runtime Environment
3. **Execution Results** → Observations → Agent → Response
4. **Real-time Updates** → Event Stream → Frontend

---

## Repository Structure

### Root Directory Layout

```
OpenHands_myversion/
├── 📁 openhands/           # Python backend core
├── 📁 frontend/            # React web application
├── 📁 evaluation/          # Testing and benchmarking
├── 📁 microagents/         # Specialized knowledge modules
├── 📁 containers/          # Docker configurations
├── 📁 docs/               # Documentation
├── 📁 tests/              # Test suites
├── 📁 dev_config/         # Development configurations
├── 📄 pyproject.toml      # Python dependencies
├── 📄 Makefile           # Build and development commands
├── 📄 README.md          # Project overview
├── 📄 Development.md     # Development guide
└── 📄 CONTRIBUTING.md    # Contribution guidelines
```

### Key Configuration Files

- **`pyproject.toml`**: Python project configuration and dependencies
- **`Makefile`**: Automated build, test, and development commands
- **`config.template.toml`**: Template for runtime configuration
- **`docker-compose.yml`**: Multi-container Docker setup
- **`pytest.ini`**: Test configuration

---

## Technical Stack

### Backend (Python)
- **Framework**: FastAPI for REST API and WebSocket support
- **Language Model Integration**: LiteLLM for multi-provider LLM support
- **Async Processing**: Python asyncio for concurrent operations
- **Package Management**: Poetry for dependency management
- **Code Quality**: Ruff (linting), MyPy (type checking), Pre-commit hooks

### Frontend (React)
- **Framework**: React 19 with Remix SPA mode
- **Build Tool**: Vite for fast development and building
- **Styling**: Tailwind CSS for utility-first styling
- **State Management**: Redux Toolkit + TanStack Query
- **UI Components**: HeroUI component library
- **Testing**: Vitest + React Testing Library
- **Internationalization**: i18next for multi-language support

### Runtime Environments
- **Docker**: Containerized execution environment
- **E2B**: Cloud-based code execution platform
- **Modal**: Serverless compute platform
- **Local**: Direct local machine execution

### Development Tools
- **Version Control**: Git with pre-commit hooks
- **Code Formatting**: Prettier (frontend), Ruff (backend)
- **Type Checking**: TypeScript (frontend), MyPy (backend)
- **Testing**: Vitest (frontend), Pytest (backend)
- **Documentation**: Markdown with automated generation

---

## Key Components Deep Dive

### 1. Backend Core (`openhands/`)

#### Agent Hub (`openhands/agenthub/`)
Contains different agent implementations:

- **CodeAct Agent**: Main general-purpose agent
  - Uses function calling interface
  - Supports bash, Python, web browsing, file editing
  - Based on CodeAct research paper

- **Browsing Agent**: Specialized for web interactions
- **Dummy Agent**: Simple agent for testing
- **LOC Agent**: Lines-of-code focused agent
- **Visual Browsing Agent**: Handles visual web elements

#### Controller (`openhands/controller/`)
Manages agent lifecycle and execution:

- **Agent Controller**: Orchestrates agent execution
- **State Management**: Maintains conversation and execution state
- **Action Parser**: Converts LLM responses to actions
- **Replay System**: Allows replaying previous sessions

#### Events (`openhands/events/`)
Event-driven communication system:

- **Actions**: Commands agents can execute
  - `CmdRunAction`: Execute bash commands
  - `FileReadAction`/`FileWriteAction`: File operations
  - `BrowseURLAction`: Web browsing
  - `IPythonRunCellAction`: Python code execution

- **Observations**: Results from action execution
  - `CmdOutputObservation`: Command results
  - `FileReadObservation`: File contents
  - `BrowserOutputObservation`: Web page data

#### Runtime (`openhands/runtime/`)
Execution environment management:

- **Base Runtime**: Abstract interface for all runtimes
- **Docker Runtime**: Containerized execution
- **E2B Runtime**: Cloud-based execution
- **Modal Runtime**: Serverless execution
- **Action Execution Server**: REST API for runtime operations

#### Server (`openhands/server/`)
Web server and API:

- **FastAPI Application**: Main web server
- **WebSocket Support**: Real-time communication
- **Session Management**: User session handling
- **Authentication**: User authentication system
- **File Management**: File upload/download handling

#### LLM Integration (`openhands/llm/`)
Language model integration:

- **LiteLLM Wrapper**: Multi-provider LLM support
- **Async LLM**: Asynchronous LLM operations
- **Retry Logic**: Automatic retry on failures
- **Metrics**: LLM usage tracking
- **Function Calling**: Tool use capabilities

### 2. Frontend Application (`frontend/`)

#### Architecture
- **Remix SPA Mode**: Single-page application with React Router
- **Component Structure**: Feature-based organization
- **State Management**: Redux for global state, TanStack Query for server state
- **Real-time Updates**: WebSocket integration for live updates

#### Key Features
- **Chat Interface**: Conversation with AI agents
- **File Explorer**: Browse and edit project files
- **Terminal**: Interactive command-line interface
- **Settings**: Configuration management
- **Authentication**: GitHub OAuth integration

#### Directory Structure
```
frontend/src/
├── api/           # API client methods
├── components/    # React components
├── hooks/         # Custom React hooks
├── routes/        # Page components
├── state/         # Redux store
├── types/         # TypeScript definitions
├── utils/         # Utility functions
└── i18n/          # Internationalization
```

### 3. Evaluation Framework (`evaluation/`)

#### Purpose
Comprehensive testing against industry benchmarks:

- **SWE-Bench**: Software engineering tasks
- **WebArena**: Web browsing tasks
- **HumanEval**: Code generation tasks
- **GAIA**: General AI assistant tasks

#### Components
- **Benchmark Runners**: Execute tests against agents
- **Result Analysis**: Performance metrics and visualization
- **Regression Testing**: Ensure improvements don't break existing functionality
- **Integration Tests**: End-to-end system testing

---

## Development Workflow

### 1. Initial Setup

```bash
# Clone the repository
git clone https://github.com/All-Hands-AI/OpenHands.git
cd OpenHands

# Install dependencies and build
make build

# Setup configuration
make setup-config
```

### 2. Development Commands

```bash
# Start full application
make run

# Start backend only
make start-backend

# Start frontend only
make start-frontend

# Run tests
make test

# Run linting
make lint

# Clean caches
make clean
```

### 3. Code Quality

#### Pre-commit Hooks
Automatically run on every commit:
- Code formatting (Ruff, Prettier)
- Type checking (MyPy, TypeScript)
- Linting (ESLint, Ruff)
- Test execution

#### Testing Strategy
- **Unit Tests**: Individual component testing
- **Integration Tests**: Component interaction testing
- **End-to-End Tests**: Full workflow testing
- **Benchmark Tests**: Performance evaluation

### 4. Development Environment

#### Backend Development
```bash
# Install Python dependencies
poetry install --with dev,test,runtime

# Run backend with hot reload
poetry run uvicorn openhands.server.listen:app --reload

# Run specific tests
poetry run pytest tests/unit/test_*.py
```

#### Frontend Development
```bash
# Install Node.js dependencies
cd frontend && npm install

# Start development server
npm run dev

# Run tests
npm run test

# Build for production
npm run build
```

---

## Agent System

### Agent Architecture

Agents in OpenHands follow a standardized interface:

```python
class Agent:
    def step(self, state: State) -> Action:
        """Execute one step towards the goal"""
        pass
```

### CodeAct Agent (Main Agent)

The primary agent implementation based on the CodeAct research:

#### Capabilities
1. **Code Execution**: Run Python and bash commands
2. **File Operations**: Read, write, and edit files
3. **Web Browsing**: Navigate and interact with websites
4. **Tool Integration**: Use specialized tools and APIs

#### Function Calling Interface
Uses LiteLLM's function calling to interact with tools:

```python
tools = [
    {
        "type": "function",
        "function": {
            "name": "execute_bash",
            "description": "Execute bash commands",
            "parameters": {
                "type": "object",
                "properties": {
                    "command": {"type": "string"}
                }
            }
        }
    }
]
```

#### Built-in Tools

1. **`execute_bash`**: Run Linux commands
   - Supports long-running processes
   - Background execution with output redirection
   - Interactive process handling

2. **`execute_ipython_cell`**: Python code execution
   - IPython environment with magic commands
   - Persistent variable scope
   - Package installation support

3. **`str_replace_editor`**: File editing
   - View files with line numbers
   - String-based find and replace
   - Undo functionality

4. **`browser`**: Web interaction
   - Navigate to URLs
   - Click elements and fill forms
   - Extract page content

### Agent Delegation

OpenHands supports multi-agent workflows:

- **Task Delegation**: Agents can delegate subtasks to specialized agents
- **Hierarchical Structure**: Main agent coordinates sub-agents
- **Context Sharing**: Shared state and communication between agents

### Agent State Management

The `State` object tracks:
- **Conversation History**: Messages and actions
- **Execution Context**: Current working directory, environment variables
- **Task Progress**: Completed and pending subtasks
- **Error Handling**: Failed actions and recovery strategies

---

## Runtime Environments

### 1. Docker Runtime (Default)

#### Features
- **Isolation**: Sandboxed execution environment
- **Reproducibility**: Consistent environment across deployments
- **Security**: Contained execution prevents system damage
- **Customization**: Custom Docker images for specific needs

#### Configuration
```toml
[runtime]
type = "docker"
container_image = "docker.all-hands.dev/all-hands-ai/runtime:latest"
```

#### Architecture
```
┌─────────────────┐    ┌─────────────────┐
│   OpenHands     │    │   Docker        │
│   Backend       │◄──►│   Container     │
└─────────────────┘    └─────────────────┘
         │                       │
         │              ┌─────────────────┐
         └─────────────►│  Action Exec    │
                        │  Server (REST)  │
                        └─────────────────┘
```

### 2. E2B Runtime

#### Features
- **Cloud-based**: No local Docker required
- **Scalable**: Automatic scaling based on demand
- **Fast Startup**: Quick environment provisioning
- **Managed**: Fully managed infrastructure

#### Use Cases
- Production deployments
- High-scale applications
- Teams without Docker expertise

### 3. Modal Runtime

#### Features
- **Serverless**: Pay-per-use execution
- **GPU Support**: Access to GPU resources
- **Auto-scaling**: Automatic resource management
- **Cost-effective**: Only pay for actual usage

### 4. Local Runtime

#### Features
- **Direct Execution**: Run commands on host machine
- **No Overhead**: Minimal performance impact
- **Development**: Ideal for development and testing

#### Security Considerations
- **Risk**: Direct access to host system
- **Use Case**: Trusted environments only
- **Isolation**: Limited security boundaries

---

## Frontend Application

### Architecture Overview

The frontend is a modern React application built with:

#### Core Technologies
- **React 19**: Latest React features and performance improvements
- **Remix SPA Mode**: File-based routing with data loading
- **Vite**: Fast build tool and development server
- **TypeScript**: Type safety and better developer experience

#### State Management Strategy

1. **Redux Toolkit**: Global application state
   - User authentication
   - Application settings
   - Chat conversation state

2. **TanStack Query**: Server state management
   - API data caching
   - Background updates
   - Optimistic updates

3. **Local State**: Component-specific state
   - Form inputs
   - UI interactions
   - Temporary data

#### Component Architecture

```
src/components/
├── features/          # Domain-specific components
│   ├── chat/         # Chat interface
│   ├── file-explorer/ # File management
│   ├── terminal/     # Command interface
│   └── settings/     # Configuration
├── layout/           # Layout components
├── modals/           # Modal dialogs
└── ui/              # Reusable UI components
```

#### Key Features

1. **Real-time Chat Interface**
   - WebSocket connection for live updates
   - Message history and persistence
   - File attachment support
   - Code syntax highlighting

2. **Integrated File Explorer**
   - Browse project files and directories
   - File editing with Monaco Editor
   - File upload and download
   - Git integration

3. **Terminal Interface**
   - Interactive command-line interface
   - Command history and autocomplete
   - Real-time output streaming
   - Process management

4. **Settings Management**
   - LLM provider configuration
   - Runtime environment selection
   - User preferences
   - Authentication settings

#### Internationalization (i18n)

- **Multi-language Support**: English, Chinese, Spanish, French, etc.
- **Dynamic Loading**: Language files loaded on demand
- **Type Safety**: TypeScript definitions for translation keys
- **Fallback System**: Graceful handling of missing translations

#### Testing Strategy

1. **Unit Tests**: Individual component testing
   ```typescript
   import { render, screen } from '@testing-library/react';
   import { ChatInput } from './chat-input';

   test('renders chat input', () => {
     render(<ChatInput />);
     expect(screen.getByRole('textbox')).toBeInTheDocument();
   });
   ```

2. **Integration Tests**: Component interaction testing
3. **E2E Tests**: Full user workflow testing with Playwright
4. **Visual Tests**: Screenshot comparison testing

---

## Evaluation Framework

### Purpose and Scope

The evaluation framework provides comprehensive testing of agent capabilities across multiple domains:

#### Supported Benchmarks

1. **Software Engineering**
   - **SWE-Bench**: Real-world GitHub issues
   - **HumanEvalFix**: Code debugging tasks
   - **BIRD**: Database query generation
   - **ML-Bench**: Machine learning tasks

2. **Web Browsing**
   - **WebArena**: Complex web navigation
   - **MiniWob++**: Simple web tasks
   - **Visual WebArena**: Visual web interaction

3. **General Assistance**
   - **GAIA**: General AI assistant tasks
   - **GPQA**: Graduate-level questions
   - **AgentBench**: Multi-domain evaluation

### Evaluation Process

#### 1. Benchmark Setup
```bash
# Install evaluation dependencies
poetry install --with evaluation

# Configure LLM for evaluation
export EVAL_LLM_CONFIG="gpt-4o"

# Run specific benchmark
python evaluation/benchmarks/swe_bench/run_infer.py
```

#### 2. Agent Testing
- **Automated Execution**: Agents run against benchmark tasks
- **Result Collection**: Performance metrics and outputs
- **Error Analysis**: Failure modes and debugging
- **Comparison**: Performance against baselines

#### 3. Result Analysis
- **Success Rates**: Percentage of tasks completed successfully
- **Performance Metrics**: Time to completion, resource usage
- **Error Categorization**: Types of failures and their frequency
- **Improvement Tracking**: Progress over time

#### 4. Visualization
- **HuggingFace Space**: Interactive result visualization
- **Comparative Analysis**: Performance across different models
- **Trend Analysis**: Performance improvements over time

### Benchmark Implementation

Each benchmark follows a standard structure:

```
evaluation/benchmarks/benchmark_name/
├── run_infer.py      # Main execution script
├── eval.py           # Evaluation logic
├── utils.py          # Helper functions
├── scripts/          # Automation scripts
└── README.md         # Benchmark documentation
```

#### Example: SWE-Bench

SWE-Bench tests agents on real GitHub issues:

1. **Task Setup**: Clone repository, checkout specific commit
2. **Agent Execution**: Agent attempts to fix the issue
3. **Validation**: Run tests to verify the fix
4. **Scoring**: Success/failure based on test results

---

## Microagents System

### Concept and Purpose

Microagents are specialized knowledge modules that enhance OpenHands with domain-specific expertise:

#### Types of Microagents

1. **Knowledge Agents**: Triggered by keywords
   - Language-specific best practices
   - Framework guidelines
   - Tool usage patterns

2. **Repository Agents**: Project-specific guidance
   - Team conventions
   - Setup instructions
   - Workflow documentation

### Microagent Structure

#### YAML Frontmatter
```yaml
---
name: github
type: knowledge
version: 1.0.0
agent: CodeActAgent
triggers:
- github
- git
---
```

#### Content Format
Microagents use Markdown with Jinja2 templating:

```markdown
# GitHub Operations

You have access to `GITHUB_TOKEN` for API operations.

## Best Practices
- Always use GitHub API instead of web browser
- Use `create_pr` tool for pull requests
- Never push directly to main branch

## Example Usage
```bash
curl -H "Authorization: token $GITHUB_TOKEN" \
     https://api.github.com/repos/owner/repo
```
```

### Loading and Activation

#### Knowledge Agents
- **Trigger-based**: Activated by keywords in conversation
- **Context-aware**: Provide relevant advice based on file types
- **Reusable**: Knowledge applicable across projects

#### Repository Agents
- **Auto-loaded**: Automatically activated for specific repositories
- **Project-specific**: Contains repository-unique guidelines
- **Team-focused**: Enforces team conventions

### Examples

#### GitHub Microagent
```markdown
---
name: github
triggers: [github, git]
---

## GitHub Operations
- Use GitHub API with GITHUB_TOKEN
- Create PRs with create_pr tool
- Never push to main branch directly
```

#### Repository Agent
```markdown
# Project Setup

## Development Environment
- Python 3.12 required
- Use Poetry for dependency management
- Run `make build` for initial setup

## Testing
- Unit tests: `pytest tests/unit/`
- Integration tests: `pytest tests/integration/`
- Frontend tests: `cd frontend && npm test`
```

---

## Configuration and Setup

### Environment Configuration

#### Core Configuration (`config.toml`)
```toml
[core]
workspace_base = "./workspace"
max_iterations = 100

[llm]
model = "gpt-4o"
api_key = "your-api-key"
base_url = "https://api.openai.com/v1"
temperature = 0.0

[runtime]
type = "docker"
container_image = "docker.all-hands.dev/all-hands-ai/runtime:latest"

[security]
enable_auto_lint = true
confirmation_mode = false
```

#### Environment Variables

**Backend Configuration**
- `SANDBOX_RUNTIME_CONTAINER_IMAGE`: Docker image for runtime
- `LOG_ALL_EVENTS`: Enable comprehensive logging
- `DEBUG`: Enable debug mode
- `GITHUB_TOKEN`: GitHub API access

**Frontend Configuration**
- `VITE_BACKEND_HOST`: Backend server address
- `VITE_USE_TLS`: Enable HTTPS/WSS
- `VITE_FRONTEND_PORT`: Frontend server port
- `VITE_MOCK_API`: Enable API mocking for development

### Development Setup

#### Prerequisites
- **Python 3.12**: Core runtime requirement
- **Node.js 22+**: Frontend development
- **Docker**: Container runtime
- **Poetry**: Python dependency management
- **Git**: Version control

#### Quick Start
```bash
# 1. Clone repository
git clone https://github.com/All-Hands-AI/OpenHands.git
cd OpenHands

# 2. Build project
make build

# 3. Configure LLM
make setup-config

# 4. Run application
make run
```

#### Development Mode
```bash
# Backend development
make start-backend

# Frontend development (separate terminal)
make start-frontend

# Run tests
make test

# Code quality checks
make lint
```

### Production Deployment

#### Docker Deployment
```bash
# Pull latest images
docker pull docker.all-hands.dev/all-hands-ai/openhands:latest
docker pull docker.all-hands.dev/all-hands-ai/runtime:latest

# Run with Docker Compose
docker-compose up -d
```

#### Cloud Deployment
- **OpenHands Cloud**: Managed hosting service
- **E2B Integration**: Cloud runtime environment
- **Modal Deployment**: Serverless execution

#### Security Considerations
- **Network Isolation**: Restrict container network access
- **Resource Limits**: Set memory and CPU constraints
- **Authentication**: Enable user authentication
- **HTTPS**: Use TLS for production deployments

---

## Testing Strategy

### Testing Philosophy

OpenHands employs a comprehensive testing strategy across multiple levels:

#### 1. Unit Testing
**Purpose**: Test individual components in isolation

**Backend (Python)**
```python
# Example: Testing agent action parsing
def test_action_parser():
    parser = ActionParser()
    action = parser.parse("execute_bash", {"command": "ls -la"})
    assert isinstance(action, CmdRunAction)
    assert action.command == "ls -la"
```

**Frontend (TypeScript)**
```typescript
// Example: Testing React component
import { render, screen } from '@testing-library/react';
import { ChatInput } from './chat-input';

test('submits message on enter', async () => {
  const onSubmit = vi.fn();
  render(<ChatInput onSubmit={onSubmit} />);

  const input = screen.getByRole('textbox');
  await userEvent.type(input, 'Hello{enter}');

  expect(onSubmit).toHaveBeenCalledWith('Hello');
});
```

#### 2. Integration Testing
**Purpose**: Test component interactions and workflows

**API Integration**
```python
def test_agent_execution_flow():
    # Test complete agent execution cycle
    agent = CodeActAgent()
    state = State()

    # Execute action
    action = agent.step(state)
    observation = runtime.execute(action)

    # Verify results
    assert observation.success
    assert "expected_output" in observation.content
```

**Frontend Integration**
```typescript
test('chat flow integration', async () => {
  render(<App />);

  // Send message
  const input = screen.getByRole('textbox');
  await userEvent.type(input, 'Create a Python script');
  await userEvent.click(screen.getByRole('button', { name: 'Send' }));

  // Verify response
  await waitFor(() => {
    expect(screen.getByText(/Creating Python script/)).toBeInTheDocument();
  });
});
```

#### 3. End-to-End Testing
**Purpose**: Test complete user workflows

**Playwright E2E Tests**
```typescript
test('complete development workflow', async ({ page }) => {
  await page.goto('http://localhost:3000');

  // Login and setup
  await page.click('[data-testid="login-button"]');
  await page.fill('[data-testid="api-key"]', 'test-key');

  // Create new project
  await page.click('[data-testid="new-project"]');
  await page.fill('[data-testid="project-name"]', 'Test Project');

  // Send development task
  await page.fill('[data-testid="chat-input"]', 'Create a simple web server');
  await page.click('[data-testid="send-button"]');

  // Verify agent response
  await expect(page.locator('[data-testid="agent-response"]')).toContainText('web server');
});
```

#### 4. Performance Testing
**Purpose**: Ensure system performance under load

**Load Testing**
```python
import asyncio
import aiohttp

async def test_concurrent_requests():
    async with aiohttp.ClientSession() as session:
        tasks = []
        for i in range(100):
            task = session.post('/api/chat', json={'message': f'Task {i}'})
            tasks.append(task)

        responses = await asyncio.gather(*tasks)

        # Verify all requests succeeded
        for response in responses:
            assert response.status == 200
```

### Test Organization

#### Backend Tests (`tests/`)
```
tests/
├── unit/              # Unit tests
│   ├── test_agents.py
│   ├── test_runtime.py
│   └── test_llm.py
├── integration/       # Integration tests
│   ├── test_api.py
│   └── test_workflows.py
└── conftest.py       # Test configuration
```

#### Frontend Tests (`frontend/__tests__/`)
```
__tests__/
├── components/        # Component tests
├── hooks/            # Custom hook tests
├── utils/            # Utility function tests
└── e2e/              # End-to-end tests
```

### Test Execution

#### Running Tests
```bash
# Backend tests
poetry run pytest tests/unit/
poetry run pytest tests/integration/

# Frontend tests
cd frontend
npm run test
npm run test:e2e

# All tests
make test
```

#### Continuous Integration
Tests run automatically on:
- **Pre-commit**: Unit tests and linting
- **Pull Requests**: Full test suite
- **Main Branch**: Complete test suite + benchmarks

#### Test Coverage
```bash
# Backend coverage
poetry run pytest --cov=openhands tests/

# Frontend coverage
cd frontend
npm run test:coverage
```

### Mock Service Worker (MSW)

The frontend uses MSW for API mocking during development and testing:

#### Setup
```typescript
// mocks/handlers.ts
export const handlers = [
  rest.post('/api/chat', (req, res, ctx) => {
    return res(
      ctx.json({
        message: 'Mocked response',
        timestamp: Date.now()
      })
    );
  })
];
```

#### Usage in Tests
```typescript
import { server } from '../mocks/server';

beforeAll(() => server.listen());
afterEach(() => server.resetHandlers());
afterAll(() => server.close());
```

---

## Deployment Options

### 1. Local Development

#### Quick Start
```bash
# Clone and setup
git clone https://github.com/All-Hands-AI/OpenHands.git
cd OpenHands
make build

# Configure
make setup-config

# Run
make run
```

#### Development Mode
```bash
# Backend only
make start-backend

# Frontend only
make start-frontend

# With hot reload
make run
```

### 2. Docker Deployment

#### Single Container
```bash
docker run -it --rm \
  -e SANDBOX_RUNTIME_CONTAINER_IMAGE=docker.all-hands.dev/all-hands-ai/runtime:latest \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v ~/.openhands-state:/.openhands-state \
  -p 3000:3000 \
  docker.all-hands.dev/all-hands-ai/openhands:latest
```

#### Docker Compose
```yaml
# docker-compose.yml
version: '3.8'
services:
  openhands:
    image: docker.all-hands.dev/all-hands-ai/openhands:latest
    ports:
      - "3000:3000"
    environment:
      - SANDBOX_RUNTIME_CONTAINER_IMAGE=docker.all-hands.dev/all-hands-ai/runtime:latest
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
      - openhands-state:/.openhands-state

volumes:
  openhands-state:
```

### 3. Cloud Deployment

#### OpenHands Cloud
- **Managed Service**: Fully managed hosting
- **Free Credits**: $50 for new users
- **Scalable**: Automatic scaling
- **Secure**: Enterprise-grade security

#### E2B Runtime
```toml
[runtime]
type = "e2b"
api_key = "your-e2b-api-key"
```

#### Modal Runtime
```toml
[runtime]
type = "modal"
token_id = "your-modal-token-id"
token_secret = "your-modal-token-secret"
```

### 4. Production Considerations

#### Security
```bash
# Hardened Docker installation
docker run -it --rm \
  --network none \
  --security-opt no-new-privileges \
  --cap-drop ALL \
  -e SANDBOX_RUNTIME_CONTAINER_IMAGE=docker.all-hands.dev/all-hands-ai/runtime:latest \
  docker.all-hands.dev/all-hands-ai/openhands:latest
```

#### Monitoring
- **Logging**: Structured logging with JSON format
- **Metrics**: Prometheus metrics for monitoring
- **Health Checks**: Built-in health check endpoints
- **Error Tracking**: Integration with error tracking services

#### Scaling
- **Horizontal Scaling**: Multiple container instances
- **Load Balancing**: Distribute requests across instances
- **Database**: External database for session storage
- **Caching**: Redis for session and data caching

### 5. Environment-Specific Configurations

#### Development
```toml
[core]
debug = true
log_level = "DEBUG"

[runtime]
type = "local"
```

#### Staging
```toml
[core]
debug = false
log_level = "INFO"

[runtime]
type = "docker"
container_image = "staging-runtime:latest"
```

#### Production
```toml
[core]
debug = false
log_level = "WARNING"

[runtime]
type = "e2b"
api_key = "${E2B_API_KEY}"

[security]
enable_auth = true
require_https = true
```

---

## Contributing Guidelines

### Getting Started

#### 1. Fork and Clone
```bash
# Fork the repository on GitHub
# Then clone your fork
git clone https://github.com/YOUR_USERNAME/OpenHands.git
cd OpenHands

# Add upstream remote
git remote add upstream https://github.com/All-Hands-AI/OpenHands.git
```

#### 2. Setup Development Environment
```bash
# Install dependencies
make build

# Install pre-commit hooks
make install-pre-commit-hooks

# Create feature branch
git checkout -b feature/your-feature-name
```

### Development Workflow

#### 1. Code Changes
```bash
# Make your changes
# Run tests
make test

# Run linting
make lint

# Commit changes
git add .
git commit -m "feat: add new feature"
```

#### 2. Pre-commit Hooks
Automatically run on every commit:
- **Ruff**: Python code formatting and linting
- **MyPy**: Python type checking
- **Prettier**: Frontend code formatting
- **ESLint**: Frontend linting
- **Tests**: Unit test execution

#### 3. Pull Request Process

**PR Title Format**
```
<type>(<scope>): <description>

Examples:
feat(agent): add new browsing capabilities
fix(frontend): resolve chat input bug
docs(readme): update installation instructions
```

**PR Description Template**
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
- [ ] Unit tests pass
- [ ] Integration tests pass
- [ ] Manual testing completed

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Documentation updated
- [ ] Tests added/updated
```

### Code Quality Standards

#### Python (Backend)
```python
# Type hints required
def process_action(action: Action) -> Observation:
    """Process an action and return observation.

    Args:
        action: The action to process

    Returns:
        The resulting observation
    """
    pass

# Docstrings for public functions
# Error handling
# Logging for debugging
```

#### TypeScript (Frontend)
```typescript
// Interfaces for type safety
interface ChatMessage {
  id: string;
  content: string;
  timestamp: number;
  sender: 'user' | 'agent';
}

// Proper error handling
const handleSubmit = async (message: string) => {
  try {
    await sendMessage(message);
  } catch (error) {
    console.error('Failed to send message:', error);
    showErrorToast('Failed to send message');
  }
};
```

### Testing Requirements

#### New Features
- **Unit Tests**: Test individual components
- **Integration Tests**: Test feature workflows
- **Documentation**: Update relevant docs
- **Examples**: Provide usage examples

#### Bug Fixes
- **Regression Tests**: Prevent future occurrences
- **Root Cause Analysis**: Document the issue
- **Validation**: Verify fix works correctly

### Documentation Standards

#### Code Documentation
- **Docstrings**: All public functions and classes
- **Type Hints**: Complete type annotations
- **Comments**: Explain complex logic
- **Examples**: Usage examples in docstrings

#### User Documentation
- **README Updates**: Keep installation instructions current
- **API Documentation**: Document new endpoints
- **User Guides**: Step-by-step instructions
- **Troubleshooting**: Common issues and solutions

### Community Guidelines

#### Communication
- **Slack**: Join #general for discussions
- **GitHub Issues**: Bug reports and feature requests
- **Discord**: Community support and questions

#### Code of Conduct
- **Respectful**: Treat all contributors with respect
- **Inclusive**: Welcome diverse perspectives
- **Constructive**: Provide helpful feedback
- **Professional**: Maintain professional standards

#### Recognition
- **Contributors**: Listed in CREDITS.md
- **Significant Contributions**: Special recognition
- **Mentorship**: Help new contributors

---

## Conclusion

OpenHands represents a sophisticated platform for AI-powered software development, combining:

### Key Strengths
1. **Modular Architecture**: Clean separation of concerns
2. **Extensible Design**: Easy to add new capabilities
3. **Comprehensive Testing**: Multiple levels of validation
4. **Developer-Friendly**: Excellent development experience
5. **Production-Ready**: Scalable deployment options

### Learning Path for Beginners

1. **Start with Setup**: Follow the quick start guide
2. **Explore the UI**: Understand the user interface
3. **Read the Code**: Study the agent implementations
4. **Run Tests**: Understand the testing framework
5. **Make Changes**: Start with small improvements
6. **Contribute**: Join the community and contribute

### Future Directions

OpenHands continues to evolve with:
- **New Agent Types**: Specialized agents for different domains
- **Enhanced Capabilities**: More tools and integrations
- **Better Performance**: Optimization and scaling improvements
- **Broader Ecosystem**: Integration with more platforms and services

This comprehensive guide provides the foundation for understanding and contributing to OpenHands. Whether you're a beginner looking to learn about AI agents or an experienced developer wanting to contribute, OpenHands offers a rich platform for exploration and innovation in AI-powered software development.

---

*This report was generated to provide a comprehensive understanding of the OpenHands codebase and architecture. For the most up-to-date information, always refer to the official documentation and repository.*
