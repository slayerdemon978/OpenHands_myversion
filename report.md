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
17. [Advanced Topics](#advanced-topics)
18. [Performance Optimization](#performance-optimization)
19. [Security Considerations](#security-considerations)
20. [Troubleshooting Guide](#troubleshooting-guide)
21. [API Reference](#api-reference)
22. [Extension Development](#extension-development)

---

## Project Overview

### What is OpenHands?

OpenHands (formerly OpenDevin) is a **revolutionary AI-powered software development platform** that represents the cutting edge of autonomous programming. Named after the concept of "open hands" - ready to help and build, this platform enables intelligent AI agents to perform complex software development tasks with minimal human intervention.

#### The Vision
OpenHands aims to democratize software development by making it accessible to everyone, regardless of their technical background. It's designed to be:
- **Intelligent**: Uses advanced LLMs to understand context and make smart decisions
- **Autonomous**: Can work independently on complex, multi-step tasks
- **Collaborative**: Works alongside human developers as a pair programming partner
- **Educational**: Helps users learn by showing its reasoning and approach

#### Core Capabilities

**1. Code Generation and Modification**
- Writes complete applications from scratch
- Refactors existing codebases for better performance
- Implements new features based on natural language descriptions
- Fixes bugs by analyzing error messages and stack traces
- Optimizes code for performance and readability

**2. System Administration**
- Configures development environments
- Manages dependencies and package installations
- Sets up CI/CD pipelines
- Handles deployment configurations
- Monitors system performance

**3. Web Interaction and Research**
- Browses documentation and Stack Overflow for solutions
- Interacts with web APIs and services
- Scrapes data from websites when needed
- Validates information from multiple sources
- Downloads and analyzes external resources

**4. Project Management**
- Creates project structures and scaffolding
- Manages version control with Git
- Creates and manages GitHub/GitLab issues and PRs
- Writes comprehensive documentation
- Maintains project roadmaps and task lists

**5. Testing and Quality Assurance**
- Writes unit, integration, and end-to-end tests
- Performs code reviews and suggests improvements
- Runs security audits and vulnerability scans
- Validates code against best practices
- Generates test reports and coverage analysis

### Key Features

#### 1. **Multi-Agent Architecture**
OpenHands employs a sophisticated multi-agent system where different agents specialize in different tasks:
- **CodeAct Agent**: General-purpose programming agent
- **Browsing Agent**: Web interaction specialist
- **Planner Agent**: Task decomposition and planning
- **Verifier Agent**: Code validation and testing
- **Delegator Agent**: Coordinates between different agents

#### 2. **Advanced Language Model Integration**
- **Multi-Provider Support**: Works with OpenAI, Anthropic, Google, and local models
- **Function Calling**: Uses structured tool calling for precise actions
- **Context Management**: Intelligent memory management for long conversations
- **Streaming Responses**: Real-time response generation
- **Cost Optimization**: Smart model selection based on task complexity

#### 3. **Comprehensive Runtime Support**
- **Docker Integration**: Isolated, reproducible environments
- **Cloud Execution**: E2B, Modal, and other cloud platforms
- **Local Development**: Direct local machine execution
- **Hybrid Deployments**: Mix of local and cloud resources
- **Custom Runtimes**: Extensible runtime architecture

#### 4. **Professional Development Tools**
- **IDE Integration**: Monaco Editor with full language support
- **Terminal Access**: Full bash/zsh terminal with history
- **File Management**: Complete file system operations
- **Git Integration**: Full version control capabilities
- **Package Management**: Support for npm, pip, cargo, etc.

#### 5. **Enterprise-Grade Features**
- **Authentication**: OAuth integration with GitHub, Google
- **Team Collaboration**: Shared workspaces and projects
- **Audit Logging**: Comprehensive action tracking
- **Role-Based Access**: Fine-grained permission control
- **API Access**: RESTful API for integration

### Target Users and Use Cases

#### **Individual Developers**
- **Rapid Prototyping**: Quickly build MVPs and proof-of-concepts
- **Learning**: Understand new technologies and frameworks
- **Code Review**: Get AI-powered code analysis and suggestions
- **Bug Fixing**: Automated debugging and issue resolution
- **Documentation**: Generate comprehensive project documentation

#### **Development Teams**
- **Code Standardization**: Enforce coding standards across projects
- **Onboarding**: Help new team members understand codebases
- **Technical Debt**: Systematically address legacy code issues
- **Testing**: Automated test generation and maintenance
- **DevOps**: Infrastructure as code and deployment automation

#### **Engineering Managers**
- **Project Planning**: Break down complex features into tasks
- **Code Quality**: Maintain high standards across the team
- **Resource Optimization**: Identify bottlenecks and inefficiencies
- **Risk Assessment**: Analyze potential issues before deployment
- **Team Productivity**: Automate repetitive tasks

#### **Educators and Students**
- **Interactive Learning**: Learn programming through guided examples
- **Assignment Help**: Get explanations and hints for coding problems
- **Project Development**: Build portfolio projects with AI assistance
- **Code Explanation**: Understand complex algorithms and patterns
- **Best Practices**: Learn industry-standard development practices

#### **Researchers and Academics**
- **Experiment Automation**: Automate research experiment setup
- **Data Analysis**: Generate analysis scripts and visualizations
- **Paper Implementation**: Implement algorithms from research papers
- **Reproducibility**: Create reproducible research environments
- **Collaboration**: Share and validate research code

### Industry Impact

#### **Productivity Gains**
- **10x Faster Development**: Rapid prototyping and implementation
- **Reduced Context Switching**: AI handles routine tasks
- **24/7 Availability**: Continuous development without breaks
- **Consistent Quality**: Standardized code patterns and practices
- **Knowledge Transfer**: Instant access to best practices

#### **Cost Reduction**
- **Lower Development Costs**: Fewer developer hours needed
- **Reduced Training Time**: AI provides instant expertise
- **Faster Time-to-Market**: Accelerated development cycles
- **Lower Maintenance Costs**: Better code quality from the start
- **Reduced Technical Debt**: Proactive code improvement

#### **Innovation Enablement**
- **Rapid Experimentation**: Quick testing of new ideas
- **Cross-Domain Knowledge**: AI brings expertise from multiple fields
- **Pattern Recognition**: Identifies optimization opportunities
- **Automated Refactoring**: Continuous code improvement
- **Emerging Technology Adoption**: Quick adaptation to new tools

### Technical Philosophy

#### **Open Source First**
OpenHands is built on the principle that AI development tools should be:
- **Transparent**: Open source code for full visibility
- **Extensible**: Plugin architecture for customization
- **Community-Driven**: Contributions from global developers
- **Standards-Based**: Following industry best practices
- **Vendor-Neutral**: Not locked to any specific provider

#### **AI Safety and Ethics**
- **Human Oversight**: Humans remain in control of critical decisions
- **Explainable AI**: Clear reasoning for all actions taken
- **Privacy Protection**: Local execution options for sensitive code
- **Bias Mitigation**: Diverse training data and evaluation
- **Responsible Use**: Guidelines for ethical AI development

#### **Performance and Scalability**
- **Efficient Resource Usage**: Optimized for minimal computational overhead
- **Horizontal Scaling**: Supports multiple concurrent users
- **Caching Strategies**: Intelligent caching for faster responses
- **Load Balancing**: Distributed processing capabilities
- **Monitoring**: Comprehensive performance metrics

---

## Core Concepts

Understanding OpenHands requires grasping several fundamental concepts that form the foundation of its architecture. These concepts work together to create a powerful, flexible, and extensible AI development platform.

### 1. Agents: The AI Workforce

**Agents** are autonomous AI entities that serve as the primary workforce in OpenHands. Think of them as specialized AI developers, each with unique skills and capabilities.

#### Agent Characteristics
- **Autonomous Decision Making**: Agents can analyze situations and choose appropriate actions without constant human guidance
- **Goal-Oriented Behavior**: Each agent works towards completing specific objectives
- **Learning Capability**: Agents improve their performance based on feedback and experience
- **Specialization**: Different agents excel in different domains (coding, web browsing, testing, etc.)
- **Collaboration**: Agents can work together and delegate tasks to each other

#### Agent Lifecycle
```python
class Agent:
    def __init__(self, llm_config, tools):
        self.llm = LLM(llm_config)
        self.tools = tools
        self.memory = ConversationMemory()

    def step(self, state: State) -> Action:
        # 1. Analyze current state
        context = self.analyze_state(state)

        # 2. Generate plan
        plan = self.create_plan(context)

        # 3. Select next action
        action = self.select_action(plan, state)

        # 4. Update memory
        self.memory.add_action(action)

        return action

    def process_observation(self, observation: Observation):
        # Learn from the result of actions
        self.memory.add_observation(observation)
        self.update_understanding(observation)
```

#### Types of Agents

**1. CodeAct Agent (Primary)**
- **Purpose**: General-purpose software development
- **Capabilities**: Code writing, debugging, testing, documentation
- **Tools**: Bash, Python, file editing, web browsing
- **Use Cases**: Full-stack development, bug fixes, feature implementation

**2. Browsing Agent**
- **Purpose**: Web interaction and research
- **Capabilities**: Navigate websites, extract information, interact with web forms
- **Tools**: Browser automation, HTML parsing, screenshot analysis
- **Use Cases**: Documentation research, API exploration, data collection

**3. Planner Agent**
- **Purpose**: Task decomposition and project planning
- **Capabilities**: Break down complex tasks, create roadmaps, estimate effort
- **Tools**: Project management, dependency analysis, timeline creation
- **Use Cases**: Project planning, sprint planning, architecture design

**4. Verifier Agent**
- **Purpose**: Quality assurance and validation
- **Capabilities**: Code review, testing, security analysis
- **Tools**: Static analysis, test execution, security scanners
- **Use Cases**: Code review, test validation, security audits

### 2. Actions and Observations: The Communication Protocol

The **Action-Observation** pattern is the fundamental communication mechanism between agents and their environment.

#### Actions: What Agents Can Do

Actions represent discrete operations that agents can perform. Each action is:
- **Atomic**: Represents a single, well-defined operation
- **Serializable**: Can be converted to/from JSON for storage and transmission
- **Typed**: Strongly typed with specific parameters and validation
- **Traceable**: Logged for debugging and analysis

**Core Action Types:**

```python
# File Operations
class FileReadAction(Action):
    path: str
    view_range: Optional[Tuple[int, int]] = None

class FileWriteAction(Action):
    path: str
    content: str
    mode: str = 'w'  # 'w' for write, 'a' for append

class FileEditAction(Action):
    path: str
    old_str: str
    new_str: str

# Command Execution
class CmdRunAction(Action):
    command: str
    background: bool = False
    timeout: Optional[int] = None

# Python Execution
class IPythonRunCellAction(Action):
    code: str
    kernel_init_code: Optional[str] = None

# Web Browsing
class BrowseURLAction(Action):
    url: str
    extract_content: bool = True

# Communication
class MessageAction(Action):
    content: str
    wait_for_response: bool = False

# Agent Control
class AgentFinishAction(Action):
    outputs: Dict[str, Any]
    summary: str

class AgentDelegateAction(Action):
    agent: str
    inputs: Dict[str, Any]
```

#### Observations: Environmental Feedback

Observations provide feedback about the results of actions. They contain:
- **Success/Failure Status**: Whether the action completed successfully
- **Output Data**: Results, error messages, or other relevant information
- **Metadata**: Timing, resource usage, and other contextual information
- **Side Effects**: Any unintended consequences or additional information

**Core Observation Types:**

```python
# Command Results
class CmdOutputObservation(Observation):
    command_id: int
    command: str
    exit_code: int
    stdout: str
    stderr: str

# File Content
class FileReadObservation(Observation):
    path: str
    content: str
    size: int
    last_modified: datetime

# Web Content
class BrowserOutputObservation(Observation):
    url: str
    content: str
    status_code: int
    screenshot: Optional[str] = None

# Error Handling
class ErrorObservation(Observation):
    error_type: str
    message: str
    traceback: Optional[str] = None

# Success Confirmation
class SuccessObservation(Observation):
    message: str
    data: Optional[Dict[str, Any]] = None
```

### 3. Runtime Environment: The Execution Sandbox

The **Runtime Environment** is where agents execute their actions safely and efficiently. It provides:

#### Isolation and Security
- **Sandboxing**: Actions execute in isolated environments
- **Resource Limits**: CPU, memory, and disk usage constraints
- **Network Controls**: Restricted network access for security
- **File System Isolation**: Separate file systems for each session

#### Runtime Types and Characteristics

**1. Docker Runtime**
```yaml
# Runtime Configuration
runtime:
  type: docker
  image: "openhands/runtime:latest"
  resources:
    memory: "2GB"
    cpu: "2 cores"
  network: "restricted"
  volumes:
    - "/workspace:/workspace"
```

**2. E2B Runtime**
```python
# E2B Configuration
runtime_config = {
    "type": "e2b",
    "template": "python-dev",
    "timeout": 300,
    "auto_scale": True
}
```

**3. Local Runtime**
```python
# Local Runtime (Development Only)
runtime_config = {
    "type": "local",
    "working_directory": "/tmp/openhands",
    "environment_variables": {
        "PATH": "/usr/local/bin:/usr/bin:/bin"
    }
}
```

#### Runtime Services

**Action Execution Server**
```python
class ActionExecutionServer:
    def __init__(self, runtime_config):
        self.runtime = create_runtime(runtime_config)
        self.session_manager = SessionManager()

    async def execute_action(self, action: Action) -> Observation:
        session = self.session_manager.get_session(action.session_id)

        try:
            # Execute action in runtime environment
            result = await self.runtime.execute(action, session)

            # Create observation from result
            observation = self.create_observation(result)

            # Log execution
            self.log_execution(action, observation)

            return observation

        except Exception as e:
            return ErrorObservation(
                error_type=type(e).__name__,
                message=str(e),
                traceback=traceback.format_exc()
            )
```

### 4. Event Stream: The Central Nervous System

The **Event Stream** serves as the central communication hub for all components in OpenHands. It enables:

#### Real-time Communication
- **Publish-Subscribe Pattern**: Components can publish events and subscribe to relevant events
- **Event Ordering**: Events are processed in chronological order
- **Event Persistence**: All events are stored for replay and analysis
- **Real-time Updates**: Frontend receives live updates through WebSocket connections

#### Event Types and Flow

```python
class Event:
    id: str
    timestamp: datetime
    source: str
    type: str
    data: Dict[str, Any]

class EventStream:
    def __init__(self):
        self.subscribers = defaultdict(list)
        self.event_store = EventStore()

    def publish(self, event: Event):
        # Store event
        self.event_store.add(event)

        # Notify subscribers
        for subscriber in self.subscribers[event.type]:
            subscriber.handle_event(event)

    def subscribe(self, event_type: str, handler: Callable):
        self.subscribers[event_type].append(handler)
```

#### Event Flow Example
```
User Input → Frontend → Backend → Agent Controller → Agent
                ↓           ↓            ↓            ↓
            Event Stream ← Event ← Action Event ← Action
                ↓
            Runtime Environment
                ↓
            Observation Event → Event Stream → Frontend Update
```

### 5. State Management: The Memory System

**State Management** in OpenHands handles the complex task of maintaining context across long-running conversations and multi-step tasks.

#### State Components

**1. Conversation State**
```python
class ConversationState:
    messages: List[Message]
    current_task: Optional[str]
    subtasks: List[SubTask]
    context_window: int

    def add_message(self, message: Message):
        self.messages.append(message)
        self.trim_if_needed()

    def trim_if_needed(self):
        if len(self.messages) > self.context_window:
            # Use condenser to summarize old messages
            self.condense_history()
```

**2. Execution State**
```python
class ExecutionState:
    current_directory: str
    environment_variables: Dict[str, str]
    running_processes: List[Process]
    open_files: List[FileHandle]

    def update_from_observation(self, obs: Observation):
        if isinstance(obs, CmdOutputObservation):
            self.update_from_command(obs)
        elif isinstance(obs, FileWriteObservation):
            self.track_file_change(obs)
```

**3. Agent State**
```python
class AgentState:
    agent_type: str
    current_plan: Optional[Plan]
    working_memory: Dict[str, Any]
    delegate_stack: List[str]

    def delegate_to(self, agent_type: str, task: str):
        self.delegate_stack.append(agent_type)
        return DelegateAction(agent=agent_type, task=task)
```

#### Memory Management Strategies

**1. Truncation Strategy**
```python
class TruncationCondenser:
    def __init__(self, max_events: int):
        self.max_events = max_events

    def condense(self, events: List[Event]) -> List[Event]:
        if len(events) <= self.max_events:
            return events

        # Keep first few and last few events
        keep_first = self.max_events // 4
        keep_last = self.max_events - keep_first

        return events[:keep_first] + events[-keep_last:]
```

**2. LLM-Based Summarization**
```python
class LLMCondenser:
    def __init__(self, llm: LLM):
        self.llm = llm

    def condense(self, events: List[Event]) -> List[Event]:
        # Summarize middle events using LLM
        summary = self.llm.summarize_events(events[10:-10])

        # Keep important events + summary
        return (
            events[:10] +
            [SummaryEvent(content=summary)] +
            events[-10:]
        )
```

### 6. Tool System: Extending Agent Capabilities

The **Tool System** allows agents to interact with external systems and perform specialized tasks.

#### Tool Interface
```python
class Tool:
    name: str
    description: str
    parameters: Dict[str, Any]

    def execute(self, **kwargs) -> ToolResult:
        raise NotImplementedError

    def validate_parameters(self, **kwargs) -> bool:
        # Validate input parameters
        pass

class ToolResult:
    success: bool
    output: Any
    error: Optional[str] = None
    metadata: Dict[str, Any] = {}
```

#### Built-in Tools

**File System Tools**
```python
class FileSystemTool(Tool):
    def read_file(self, path: str) -> str:
        with open(path, 'r') as f:
            return f.read()

    def write_file(self, path: str, content: str):
        with open(path, 'w') as f:
            f.write(content)

    def list_directory(self, path: str) -> List[str]:
        return os.listdir(path)
```

**Command Execution Tools**
```python
class CommandTool(Tool):
    def execute_command(self, command: str, timeout: int = 30) -> CommandResult:
        process = subprocess.run(
            command,
            shell=True,
            capture_output=True,
            text=True,
            timeout=timeout
        )

        return CommandResult(
            exit_code=process.returncode,
            stdout=process.stdout,
            stderr=process.stderr
        )
```

**Web Browsing Tools**
```python
class BrowserTool(Tool):
    def __init__(self):
        self.driver = webdriver.Chrome()

    def navigate(self, url: str):
        self.driver.get(url)

    def click_element(self, selector: str):
        element = self.driver.find_element(By.CSS_SELECTOR, selector)
        element.click()

    def extract_text(self, selector: str) -> str:
        element = self.driver.find_element(By.CSS_SELECTOR, selector)
        return element.text
```

### 7. Configuration System: Flexible Setup

OpenHands uses a hierarchical configuration system that allows for flexible deployment and customization.

#### Configuration Hierarchy
1. **Default Values**: Built-in defaults for all settings
2. **Configuration File**: TOML file with user preferences
3. **Environment Variables**: Override config file settings
4. **Runtime Parameters**: Override everything for specific sessions

```python
class Config:
    def __init__(self):
        self.load_defaults()
        self.load_config_file()
        self.load_environment_variables()

    def load_defaults(self):
        self.settings = {
            "llm": {
                "model": "gpt-4",
                "temperature": 0.0,
                "max_tokens": 4096
            },
            "runtime": {
                "type": "docker",
                "timeout": 300
            },
            "security": {
                "enable_sandbox": True,
                "allow_network": False
            }
        }

    def get(self, key: str, default=None):
        keys = key.split('.')
        value = self.settings

        for k in keys:
            if k in value:
                value = value[k]
            else:
                return default

        return value
```

This comprehensive understanding of core concepts provides the foundation for working with OpenHands effectively. Each concept builds upon the others to create a powerful, flexible, and extensible AI development platform.

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

## Advanced Topics

### Multi-Agent Coordination

OpenHands supports sophisticated multi-agent workflows where different agents collaborate to solve complex problems.

#### Agent Delegation Patterns

**1. Hierarchical Delegation**
```python
class DelegatorAgent(Agent):
    def __init__(self):
        self.sub_agents = {
            'coder': CodeActAgent(),
            'browser': BrowsingAgent(),
            'tester': TestingAgent()
        }

    def step(self, state: State) -> Action:
        task_type = self.analyze_task_type(state.current_task)

        if task_type == 'web_research':
            return AgentDelegateAction(
                agent='browser',
                inputs={'query': state.current_task}
            )
        elif task_type == 'code_implementation':
            return AgentDelegateAction(
                agent='coder',
                inputs={'requirements': state.current_task}
            )
```

**2. Parallel Execution**
```python
class ParallelCoordinator:
    async def execute_parallel_tasks(self, tasks: List[Task]) -> List[Result]:
        # Execute multiple agents simultaneously
        agent_tasks = []

        for task in tasks:
            agent = self.select_agent_for_task(task)
            agent_task = asyncio.create_task(
                agent.execute_task(task)
            )
            agent_tasks.append(agent_task)

        # Wait for all tasks to complete
        results = await asyncio.gather(*agent_tasks)

        # Merge and validate results
        return self.merge_results(results)
```

#### Communication Protocols

**Agent-to-Agent Messaging**
```python
class AgentMessage:
    sender: str
    recipient: str
    message_type: str
    content: Dict[str, Any]
    timestamp: datetime

class AgentCommunicationHub:
    def __init__(self):
        self.message_queue = asyncio.Queue()
        self.agent_registry = {}

    async def send_message(self, message: AgentMessage):
        await self.message_queue.put(message)

    async def process_messages(self):
        while True:
            message = await self.message_queue.get()
            recipient = self.agent_registry.get(message.recipient)

            if recipient:
                await recipient.handle_message(message)
```

### Context Management and Memory

#### Long-Term Memory Systems

**1. Episodic Memory**
```python
class EpisodicMemory:
    def __init__(self):
        self.episodes = []
        self.embeddings = EmbeddingStore()

    def store_episode(self, episode: Episode):
        # Store episode with semantic embeddings
        embedding = self.embeddings.embed(episode.summary)

        self.episodes.append({
            'episode': episode,
            'embedding': embedding,
            'timestamp': datetime.now()
        })

    def retrieve_similar_episodes(self, query: str, k: int = 5) -> List[Episode]:
        query_embedding = self.embeddings.embed(query)

        # Find most similar episodes
        similarities = []
        for stored in self.episodes:
            similarity = cosine_similarity(query_embedding, stored['embedding'])
            similarities.append((similarity, stored['episode']))

        # Return top-k most similar
        similarities.sort(reverse=True)
        return [episode for _, episode in similarities[:k]]
```

**2. Semantic Memory**
```python
class SemanticMemory:
    def __init__(self):
        self.knowledge_graph = NetworkX.Graph()
        self.concept_embeddings = {}

    def add_concept(self, concept: str, properties: Dict[str, Any]):
        self.knowledge_graph.add_node(concept, **properties)
        self.concept_embeddings[concept] = self.embed_concept(concept, properties)

    def add_relationship(self, concept1: str, concept2: str, relationship: str):
        self.knowledge_graph.add_edge(concept1, concept2, type=relationship)

    def query_knowledge(self, query: str) -> List[Dict[str, Any]]:
        # Use graph traversal and embedding similarity
        relevant_concepts = self.find_relevant_concepts(query)

        results = []
        for concept in relevant_concepts:
            context = self.get_concept_context(concept)
            results.append({
                'concept': concept,
                'context': context,
                'relevance': self.calculate_relevance(query, concept)
            })

        return sorted(results, key=lambda x: x['relevance'], reverse=True)
```

#### Context Compression Strategies

**1. Hierarchical Summarization**
```python
class HierarchicalSummarizer:
    def __init__(self, llm: LLM):
        self.llm = llm
        self.summary_levels = [10, 50, 200]  # Events per level

    def compress_context(self, events: List[Event]) -> List[Event]:
        if len(events) <= self.summary_levels[0]:
            return events

        # Create hierarchical summaries
        compressed = []

        # Keep most recent events
        compressed.extend(events[-self.summary_levels[0]:])

        # Summarize middle sections
        remaining = events[:-self.summary_levels[0]]

        for level in self.summary_levels[1:]:
            if len(remaining) <= level:
                compressed = self.summarize_events(remaining) + compressed
                break

            # Summarize oldest section
            to_summarize = remaining[:-level]
            summary = self.summarize_events(to_summarize)
            compressed = summary + compressed

            remaining = remaining[-level:]

        return compressed
```

### Performance Optimization

#### Caching Strategies

**1. LLM Response Caching**
```python
class LLMCache:
    def __init__(self, cache_backend='redis'):
        self.cache = self.create_cache_backend(cache_backend)
        self.ttl = 3600  # 1 hour default TTL

    def get_cache_key(self, prompt: str, model: str, temperature: float) -> str:
        # Create deterministic cache key
        content = f"{model}:{temperature}:{prompt}"
        return hashlib.sha256(content.encode()).hexdigest()

    async def get_cached_response(self, prompt: str, model: str, temperature: float):
        cache_key = self.get_cache_key(prompt, model, temperature)

        cached = await self.cache.get(cache_key)
        if cached:
            return json.loads(cached)

        return None

    async def cache_response(self, prompt: str, model: str, temperature: float, response: str):
        cache_key = self.get_cache_key(prompt, model, temperature)

        await self.cache.setex(
            cache_key,
            self.ttl,
            json.dumps(response)
        )
```

**2. Action Result Caching**
```python
class ActionCache:
    def __init__(self):
        self.cache = {}
        self.cache_policies = {
            'FileReadAction': self.file_read_policy,
            'CmdRunAction': self.command_policy,
            'BrowseURLAction': self.browse_policy
        }

    def should_cache(self, action: Action) -> bool:
        policy = self.cache_policies.get(type(action).__name__)
        return policy(action) if policy else False

    def file_read_policy(self, action: FileReadAction) -> bool:
        # Cache file reads for files that haven't changed
        file_stat = os.stat(action.path)
        cache_key = f"{action.path}:{file_stat.st_mtime}"

        return cache_key not in self.cache

    def command_policy(self, action: CmdRunAction) -> bool:
        # Only cache deterministic, read-only commands
        safe_commands = ['ls', 'cat', 'grep', 'find', 'wc']
        command_parts = action.command.split()

        return len(command_parts) > 0 and command_parts[0] in safe_commands
```

#### Parallel Processing

**1. Concurrent Action Execution**
```python
class ConcurrentExecutor:
    def __init__(self, max_workers: int = 4):
        self.executor = ThreadPoolExecutor(max_workers=max_workers)
        self.semaphore = asyncio.Semaphore(max_workers)

    async def execute_actions_concurrently(self, actions: List[Action]) -> List[Observation]:
        # Group actions by dependency
        independent_actions = self.find_independent_actions(actions)
        dependent_actions = self.find_dependent_actions(actions)

        # Execute independent actions concurrently
        concurrent_tasks = []

        async with self.semaphore:
            for action in independent_actions:
                task = asyncio.create_task(self.execute_action(action))
                concurrent_tasks.append(task)

        # Wait for concurrent execution
        concurrent_results = await asyncio.gather(*concurrent_tasks)

        # Execute dependent actions sequentially
        dependent_results = []
        for action in dependent_actions:
            result = await self.execute_action(action)
            dependent_results.append(result)

        return concurrent_results + dependent_results
```

#### Resource Management

**1. Memory Management**
```python
class MemoryManager:
    def __init__(self, max_memory_mb: int = 1024):
        self.max_memory = max_memory_mb * 1024 * 1024
        self.current_usage = 0
        self.memory_pools = {}

    def allocate_memory(self, size: int, pool_name: str = 'default') -> bool:
        if self.current_usage + size > self.max_memory:
            # Try to free memory
            if not self.free_memory(size):
                return False

        self.current_usage += size

        if pool_name not in self.memory_pools:
            self.memory_pools[pool_name] = 0

        self.memory_pools[pool_name] += size
        return True

    def free_memory(self, target_size: int) -> bool:
        # Implement LRU eviction strategy
        freed = 0

        # Free from least recently used pools
        for pool_name in sorted(self.memory_pools.keys()):
            pool_size = self.memory_pools[pool_name]

            if freed >= target_size:
                break

            # Free entire pool
            self.current_usage -= pool_size
            freed += pool_size
            del self.memory_pools[pool_name]

        return freed >= target_size
```

## Security Considerations

### Sandboxing and Isolation

#### Container Security

**1. Docker Security Configuration**
```yaml
# Secure Docker configuration
version: '3.8'
services:
  openhands-runtime:
    image: openhands/runtime:latest
    security_opt:
      - no-new-privileges:true
      - seccomp:unconfined
    cap_drop:
      - ALL
    cap_add:
      - CHOWN
      - DAC_OVERRIDE
      - SETUID
      - SETGID
    read_only: true
    tmpfs:
      - /tmp:noexec,nosuid,size=100m
    ulimits:
      nproc: 65535
      nofile:
        soft: 65535
        hard: 65535
```

**2. Network Isolation**
```python
class NetworkSecurityManager:
    def __init__(self):
        self.allowed_domains = set()
        self.blocked_domains = set()
        self.firewall_rules = []

    def configure_network_policy(self, policy: Dict[str, Any]):
        # Configure iptables rules for container
        rules = [
            # Block all outbound by default
            "iptables -P OUTPUT DROP",

            # Allow localhost
            "iptables -A OUTPUT -d 127.0.0.1 -j ACCEPT",

            # Allow DNS
            "iptables -A OUTPUT -p udp --dport 53 -j ACCEPT",
        ]

        # Add allowed domains
        for domain in policy.get('allowed_domains', []):
            ip = self.resolve_domain(domain)
            rules.append(f"iptables -A OUTPUT -d {ip} -j ACCEPT")

        return rules
```

#### Code Execution Security

**1. Command Sanitization**
```python
class CommandSanitizer:
    def __init__(self):
        self.dangerous_commands = {
            'rm', 'rmdir', 'del', 'format', 'fdisk',
            'mkfs', 'dd', 'shutdown', 'reboot', 'halt'
        }

        self.dangerous_patterns = [
            r'rm\s+-rf\s+/',  # Recursive delete from root
            r':\(\)\{.*\}',   # Fork bomb
            r'>\s*/dev/sd',   # Write to disk devices
        ]

    def sanitize_command(self, command: str) -> Tuple[bool, str]:
        # Check for dangerous commands
        command_parts = shlex.split(command)

        if command_parts and command_parts[0] in self.dangerous_commands:
            return False, f"Dangerous command blocked: {command_parts[0]}"

        # Check for dangerous patterns
        for pattern in self.dangerous_patterns:
            if re.search(pattern, command):
                return False, f"Dangerous pattern detected: {pattern}"

        # Additional validation
        if self.contains_privilege_escalation(command):
            return False, "Privilege escalation attempt detected"

        return True, "Command approved"

    def contains_privilege_escalation(self, command: str) -> bool:
        escalation_keywords = ['sudo', 'su', 'chmod +s', 'setuid']
        return any(keyword in command.lower() for keyword in escalation_keywords)
```

**2. File Access Control**
```python
class FileAccessController:
    def __init__(self, workspace_root: str):
        self.workspace_root = os.path.abspath(workspace_root)
        self.allowed_paths = {self.workspace_root}
        self.blocked_paths = {'/etc', '/sys', '/proc', '/dev'}

    def validate_file_access(self, path: str, operation: str) -> Tuple[bool, str]:
        abs_path = os.path.abspath(path)

        # Check if path is within workspace
        if not abs_path.startswith(self.workspace_root):
            return False, f"Access denied: Path outside workspace: {abs_path}"

        # Check blocked paths
        for blocked in self.blocked_paths:
            if abs_path.startswith(blocked):
                return False, f"Access denied: Blocked path: {abs_path}"

        # Check operation permissions
        if operation == 'write' and self.is_readonly_path(abs_path):
            return False, f"Write access denied: Read-only path: {abs_path}"

        return True, "Access granted"
```

### Authentication and Authorization

#### User Authentication
```python
class AuthenticationManager:
    def __init__(self, secret_key: str):
        self.secret_key = secret_key
        self.token_expiry = 3600  # 1 hour

    def create_jwt_token(self, user_id: str, permissions: List[str]) -> str:
        payload = {
            'user_id': user_id,
            'permissions': permissions,
            'exp': datetime.utcnow() + timedelta(seconds=self.token_expiry),
            'iat': datetime.utcnow()
        }

        return jwt.encode(payload, self.secret_key, algorithm='HS256')

    def validate_token(self, token: str) -> Tuple[bool, Dict[str, Any]]:
        try:
            payload = jwt.decode(token, self.secret_key, algorithms=['HS256'])
            return True, payload
        except jwt.ExpiredSignatureError:
            return False, {'error': 'Token expired'}
        except jwt.InvalidTokenError:
            return False, {'error': 'Invalid token'}
```

#### Role-Based Access Control
```python
class RBACManager:
    def __init__(self):
        self.roles = {
            'admin': {
                'permissions': ['*'],  # All permissions
                'restrictions': []
            },
            'developer': {
                'permissions': [
                    'code.read', 'code.write', 'code.execute',
                    'file.read', 'file.write', 'terminal.access'
                ],
                'restrictions': ['no_system_files']
            },
            'viewer': {
                'permissions': ['code.read', 'file.read'],
                'restrictions': ['readonly']
            }
        }

    def check_permission(self, user_role: str, action: str, resource: str) -> bool:
        role_config = self.roles.get(user_role)
        if not role_config:
            return False

        permissions = role_config['permissions']

        # Check if user has wildcard permission
        if '*' in permissions:
            return True

        # Check specific permission
        permission_key = f"{action}.{resource}"
        return permission_key in permissions
```

## Troubleshooting Guide

### Common Issues and Solutions

#### 1. Agent Not Responding

**Symptoms:**
- Agent appears stuck or unresponsive
- No actions being generated
- Timeout errors

**Diagnosis:**
```python
class AgentDiagnostics:
    def diagnose_unresponsive_agent(self, agent: Agent, state: State) -> Dict[str, Any]:
        diagnosis = {
            'llm_connectivity': self.check_llm_connectivity(agent.llm),
            'memory_usage': self.check_memory_usage(agent),
            'context_size': len(state.history),
            'last_action_time': state.last_action_timestamp,
            'error_count': state.error_count
        }

        # Identify likely causes
        issues = []

        if not diagnosis['llm_connectivity']:
            issues.append("LLM connection failed")

        if diagnosis['memory_usage'] > 0.9:
            issues.append("High memory usage")

        if diagnosis['context_size'] > 10000:
            issues.append("Context window too large")

        diagnosis['likely_issues'] = issues
        return diagnosis
```

**Solutions:**
1. **LLM Connection Issues:**
   ```bash
   # Check API key and connectivity
   export LLM_API_KEY="your-key"
   curl -H "Authorization: Bearer $LLM_API_KEY" https://api.openai.com/v1/models
   ```

2. **Memory Issues:**
   ```python
   # Reduce context window
   config.update({
       'memory': {
           'max_events': 1000,
           'condenser_type': 'llm_summary'
       }
   })
   ```

3. **Context Window Issues:**
   ```python
   # Enable aggressive context compression
   agent.memory.enable_compression(
       strategy='hierarchical',
       compression_ratio=0.5
   )
   ```

#### 2. Runtime Environment Issues

**Docker Container Problems:**
```bash
# Check container status
docker ps -a | grep openhands

# Check container logs
docker logs openhands-runtime

# Restart container
docker restart openhands-runtime

# Check resource usage
docker stats openhands-runtime
```

**Permission Issues:**
```bash
# Fix file permissions
sudo chown -R $USER:$USER ./workspace
chmod -R 755 ./workspace

# Check Docker socket permissions
sudo chmod 666 /var/run/docker.sock
```

#### 3. Performance Issues

**Slow Response Times:**
```python
class PerformanceProfiler:
    def __init__(self):
        self.metrics = {}

    def profile_agent_step(self, agent: Agent, state: State) -> Dict[str, float]:
        start_time = time.time()

        # Profile LLM call
        llm_start = time.time()
        response = agent.llm.completion(prompt)
        llm_time = time.time() - llm_start

        # Profile action parsing
        parse_start = time.time()
        action = agent.parse_response(response)
        parse_time = time.time() - parse_start

        total_time = time.time() - start_time

        return {
            'total_time': total_time,
            'llm_time': llm_time,
            'parse_time': parse_time,
            'llm_percentage': (llm_time / total_time) * 100
        }
```

**Optimization Strategies:**
1. **Enable Caching:**
   ```python
   config.update({
       'cache': {
           'enabled': True,
           'llm_cache_ttl': 3600,
           'action_cache_size': 1000
       }
   })
   ```

2. **Use Faster Models:**
   ```python
   config.update({
       'llm': {
           'model': 'gpt-3.5-turbo',  # Faster than GPT-4
           'temperature': 0.0,
           'max_tokens': 2048
       }
   })
   ```

### Debugging Tools

#### 1. Event Stream Inspector
```python
class EventStreamInspector:
    def __init__(self, event_stream: EventStream):
        self.event_stream = event_stream
        self.filters = {}

    def inspect_events(self, time_range: Tuple[datetime, datetime]) -> List[Event]:
        events = self.event_stream.get_events_in_range(time_range)

        # Analyze event patterns
        analysis = {
            'total_events': len(events),
            'event_types': Counter(e.type for e in events),
            'error_events': [e for e in events if 'error' in e.type.lower()],
            'performance_metrics': self.calculate_performance_metrics(events)
        }

        return analysis

    def find_stuck_patterns(self, events: List[Event]) -> List[Dict[str, Any]]:
        # Identify repeated failed actions
        action_attempts = defaultdict(list)

        for event in events:
            if event.type == 'action':
                key = f"{event.data['action_type']}:{event.data.get('parameters', {})}"
                action_attempts[key].append(event)

        # Find actions attempted multiple times
        stuck_patterns = []
        for action_key, attempts in action_attempts.items():
            if len(attempts) > 3:  # More than 3 attempts
                stuck_patterns.append({
                    'action': action_key,
                    'attempts': len(attempts),
                    'first_attempt': attempts[0].timestamp,
                    'last_attempt': attempts[-1].timestamp
                })

        return stuck_patterns
```

#### 2. Agent State Visualizer
```python
class AgentStateVisualizer:
    def create_state_diagram(self, state: State) -> str:
        # Create Mermaid diagram of agent state
        diagram = ["graph TD"]

        # Add current task
        diagram.append(f"    A[Current Task: {state.current_task}]")

        # Add subtasks
        for i, subtask in enumerate(state.subtasks):
            diagram.append(f"    B{i}[Subtask {i}: {subtask.description}]")
            diagram.append(f"    A --> B{i}")

        # Add agent stack
        for i, agent in enumerate(state.delegate_stack):
            diagram.append(f"    C{i}[Agent: {agent}]")
            if i > 0:
                diagram.append(f"    C{i-1} --> C{i}")

        return "\n".join(diagram)
```

## API Reference

### Core API Endpoints

#### 1. Session Management
```python
# Create new session
POST /api/sessions
{
    "agent_type": "CodeActAgent",
    "runtime_config": {
        "type": "docker",
        "image": "openhands/runtime:latest"
    },
    "llm_config": {
        "model": "gpt-4",
        "temperature": 0.0
    }
}

# Get session status
GET /api/sessions/{session_id}

# Delete session
DELETE /api/sessions/{session_id}
```

#### 2. Agent Interaction
```python
# Send message to agent
POST /api/sessions/{session_id}/messages
{
    "content": "Create a Python web server",
    "wait_for_response": true
}

# Get conversation history
GET /api/sessions/{session_id}/history?limit=50&offset=0

# Execute specific action
POST /api/sessions/{session_id}/actions
{
    "action_type": "CmdRunAction",
    "parameters": {
        "command": "ls -la"
    }
}
```

#### 3. File Management
```python
# Upload file
POST /api/sessions/{session_id}/files
Content-Type: multipart/form-data

# Download file
GET /api/sessions/{session_id}/files/{file_path}

# List files
GET /api/sessions/{session_id}/files?path=/workspace

# Edit file
PUT /api/sessions/{session_id}/files/{file_path}
{
    "content": "file content",
    "encoding": "utf-8"
}
```

### WebSocket API

#### Real-time Updates
```javascript
// Connect to WebSocket
const ws = new WebSocket('ws://localhost:3000/ws/sessions/{session_id}');

// Handle events
ws.onmessage = (event) => {
    const data = JSON.parse(event.data);

    switch (data.type) {
        case 'action':
            console.log('Agent action:', data.action);
            break;
        case 'observation':
            console.log('Action result:', data.observation);
            break;
        case 'message':
            console.log('Agent message:', data.content);
            break;
        case 'error':
            console.error('Error:', data.error);
            break;
    }
};

// Send message
ws.send(JSON.stringify({
    type: 'message',
    content: 'Hello, agent!'
}));
```

### SDK Usage Examples

#### Python SDK
```python
from openhands import OpenHandsClient

# Initialize client
client = OpenHandsClient(
    api_key="your-api-key",
    base_url="http://localhost:3000"
)

# Create session
session = client.create_session(
    agent_type="CodeActAgent",
    runtime_config={
        "type": "docker",
        "image": "openhands/runtime:latest"
    }
)

# Send message and wait for response
response = session.send_message(
    "Create a simple web server in Python",
    wait_for_completion=True
)

print(f"Agent response: {response.content}")

# Get generated files
files = session.list_files("/workspace")
for file in files:
    print(f"Generated file: {file.path}")
```

#### JavaScript SDK
```javascript
import { OpenHandsClient } from '@openhands/sdk';

// Initialize client
const client = new OpenHandsClient({
    apiKey: 'your-api-key',
    baseUrl: 'http://localhost:3000'
});

// Create session
const session = await client.createSession({
    agentType: 'CodeActAgent',
    runtimeConfig: {
        type: 'docker',
        image: 'openhands/runtime:latest'
    }
});

// Send message with streaming response
const stream = session.sendMessageStream('Create a React component');

for await (const chunk of stream) {
    if (chunk.type === 'message') {
        console.log('Agent:', chunk.content);
    } else if (chunk.type === 'action') {
        console.log('Action:', chunk.action.type);
    }
}
```

## Extension Development

### Creating Custom Agents

#### 1. Agent Interface Implementation
```python
from openhands.controller.agent import Agent
from openhands.events.action import Action
from openhands.controller.state.state import State

class CustomAgent(Agent):
    def __init__(self, llm_config: Dict[str, Any]):
        super().__init__(llm_config)
        self.specialized_tools = self.load_specialized_tools()

    def step(self, state: State) -> Action:
        # Analyze current state
        context = self.analyze_context(state)

        # Generate specialized prompt
        prompt = self.create_specialized_prompt(context)

        # Get LLM response
        response = self.llm.completion(prompt)

        # Parse response into action
        action = self.parse_response(response)

        return action

    def create_specialized_prompt(self, context: Dict[str, Any]) -> str:
        # Create domain-specific prompt
        return f"""
        You are a specialized agent for {self.domain}.

        Current context: {context}

        Available tools: {self.get_available_tools()}

        Please analyze the situation and choose the best action.
        """

    def load_specialized_tools(self) -> List[Tool]:
        # Load domain-specific tools
        return [
            CustomTool1(),
            CustomTool2(),
            CustomTool3()
        ]
```

#### 2. Custom Tool Development
```python
from openhands.events.action import Action
from openhands.events.observation import Observation

class CustomTool:
    name = "custom_tool"
    description = "Performs custom operations"

    def __init__(self):
        self.setup_tool()

    def execute(self, **kwargs) -> Observation:
        try:
            # Perform custom operation
            result = self.perform_operation(**kwargs)

            return SuccessObservation(
                content=result,
                metadata={'tool': self.name}
            )

        except Exception as e:
            return ErrorObservation(
                error_type=type(e).__name__,
                message=str(e)
            )

    def perform_operation(self, **kwargs):
        # Implement custom logic
        pass

    def validate_parameters(self, **kwargs) -> bool:
        # Validate input parameters
        required_params = ['param1', 'param2']
        return all(param in kwargs for param in required_params)
```

### Plugin System

#### 1. Plugin Interface
```python
class Plugin:
    name: str
    version: str
    dependencies: List[str]

    def initialize(self, config: Dict[str, Any]):
        """Initialize plugin with configuration"""
        pass

    def register_tools(self) -> List[Tool]:
        """Register tools provided by this plugin"""
        return []

    def register_agents(self) -> List[Type[Agent]]:
        """Register agent types provided by this plugin"""
        return []

    def register_event_handlers(self) -> Dict[str, Callable]:
        """Register event handlers"""
        return {}

    def cleanup(self):
        """Cleanup resources when plugin is unloaded"""
        pass
```

#### 2. Plugin Manager
```python
class PluginManager:
    def __init__(self):
        self.plugins = {}
        self.plugin_registry = {}

    def load_plugin(self, plugin_path: str) -> bool:
        try:
            # Load plugin module
            spec = importlib.util.spec_from_file_location("plugin", plugin_path)
            module = importlib.util.module_from_spec(spec)
            spec.loader.exec_module(module)

            # Get plugin class
            plugin_class = getattr(module, 'Plugin')
            plugin = plugin_class()

            # Initialize plugin
            plugin.initialize(self.get_plugin_config(plugin.name))

            # Register plugin components
            self.register_plugin_components(plugin)

            self.plugins[plugin.name] = plugin
            return True

        except Exception as e:
            logger.error(f"Failed to load plugin {plugin_path}: {e}")
            return False

    def register_plugin_components(self, plugin: Plugin):
        # Register tools
        for tool in plugin.register_tools():
            self.plugin_registry[f"tool:{tool.name}"] = tool

        # Register agents
        for agent_class in plugin.register_agents():
            self.plugin_registry[f"agent:{agent_class.__name__}"] = agent_class

        # Register event handlers
        for event_type, handler in plugin.register_event_handlers().items():
            self.plugin_registry[f"handler:{event_type}"] = handler
```

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
