# Knowledge Document Templates Guide

> **Complete guide to using the 6-document template system for structured AI development**

## 🎯 Overview

The knowledge document templates transform vague project ideas into structured, AI-agent-ready specifications. This guide shows you how to use each template effectively to **maintain structural integrity** and **prevent agent conflicts**. The key insight: **60-70% of your time should be spent on these documents** before any coding begins.

## 📚 Template Overview

| Template | Purpose | When to Use | Key Output |
|----------|---------|-------------|------------|
| **FOUNDATION_KNOWLEDGE** | Project constitution | Project start | Development philosophy & constraints |
| **SCOPE_DOC** | Detailed scope | After foundation | Specific requirements & roadmap |
| **STRUCTURE_MAP** | Technical architecture | After scope | File organization & patterns |
| **REALITY_TESTS** | Testing strategy | Before implementation | Test scenarios & quality standards |
| **AGENT_PROMPT_MAP** | AI agent communication | During development | Specific prompts for each agent |
| **AGENTIC_LOGIC_GUIDE** | Intelligent system design | For AI features | Patterns & best practices |

## 🏗️ Template 1: FOUNDATION_KNOWLEDGE

### Purpose
Establishes the "constitution" of your project - the core values, constraints, and development philosophy that guide all decisions.

### When to Use
- **Before any coding begins**
- **When project scope is unclear**
- **When team members need alignment**
- **When you need to prevent scope creep**

### Key Sections

#### Build Philosophy
```markdown
## Build Philosophy
- **Simplicity First**: Keep the stack minimal (Flask + HTML/CSS/JS)
- **User-Centric**: Focus on solving real user problems
- **Performance Conscious**: Fast loading and efficient processing
- **Maintainable**: Code that's easy to understand and modify
```

#### AI Agent Roles & Division of Labor
```markdown
## AI Agent Roles & Division of Labor
- **Cursor Role**: Backend logic, API development, database integration
- **Replit Role**: Frontend components, UI design, user experience
- **ChatGPT Role**: Project planning, prompt optimization, business logic
```

#### Development Rules & Constraints
```markdown
## Development Rules & Constraints
- **Single Server**: Flask application serving both API and frontend
- **Simple Frontend**: HTML/CSS/JS only, no complex frameworks
- **Error Resilience**: Graceful handling of all failure scenarios
- **Cost Conscious**: Optimize for minimal API usage and hosting costs
```

#### What We're NOT Doing
```markdown
## What We're NOT Doing
- Complex frontend frameworks (React, Vue, Angular)
- Real-time collaboration features
- Advanced authentication systems
- Multi-language support beyond English
- Real-time data synchronization
```

### Best Practices
1. **Be Specific**: Don't say "keep it simple" - say "Flask + HTML/CSS/JS only"
2. **Set Boundaries**: Clearly define what you won't build
3. **Align with Goals**: Ensure philosophy supports your business objectives
4. **Consider Constraints**: Factor in time, budget, and technical limitations

### Example: Auto-Graph Foundation
```markdown
## Build Philosophy
- **Agent-Aware Focus**: Specifically designed for teams using AI agents
- **Enterprise Ready**: Compliance and audit capabilities built-in
- **Performance Conscious**: Fast processing with intelligent caching
- **File Preservation**: Never modify original codebase, output to separate directory

## AI Agent Roles & Division of Labor
- **Cursor Role**: AST parsing, LLM integration, graph construction, backend logic
- **Replit Role**: Web interface components, graph visualization, file upload UI
- **ChatGPT Role**: Project scoping, semantic analysis prompts, business context extraction

## What We're NOT Doing
- Real-time codebase monitoring
- Advanced graph layout algorithms
- Multi-language support beyond Python/JavaScript
- Collaborative editing features
```

## 📋 Template 2: SCOPE_DOC

### Purpose
Defines the detailed scope, requirements, and development roadmap for your project.

### When to Use
- **After FOUNDATION_KNOWLEDGE is complete**
- **When you need to break down the project into phases**
- **When stakeholders need specific deliverables**
- **When you need to estimate time and resources**

### Key Sections

#### One-line Summary
```markdown
## One-line Summary
Web-based tool that analyzes user behavior and provides personalized recommendations using AI.
```

#### What We're Building
```markdown
## What We're Building
- **Input**: User interaction data and preferences
- **Processing**: AI-powered analysis and recommendation generation
- **Output**: Personalized recommendations and insights
- **Core Logic**: Machine learning recommendation engine
```

#### What We're NOT Building
```markdown
## What We're NOT Building
- Real-time data processing
- Advanced user authentication
- Multi-platform mobile apps
- Complex data visualization dashboards
```

#### External Dependencies
```markdown
## External Dependencies
- **OpenAI API**: Recommendation generation and analysis
- **Flask**: Web framework for API and frontend serving
- **SQLite**: Local data storage (upgrade to PostgreSQL for production)
- **Free Hosting**: Render/Railway for deployment
```

#### Performance Requirements
```markdown
## Performance Requirements
- **Response Time**: ≤2 seconds for recommendation generation
- **Concurrent Users**: Support 10+ simultaneous users
- **Data Processing**: Handle 1000+ user interactions per day
- **Memory Usage**: ≤200MB for typical usage
```

#### Development Phases
```markdown
## Development Phases
1. **Phase 1**: Core recommendation engine and basic UI
2. **Phase 2**: User interface improvements and data visualization
3. **Phase 3**: Advanced features and optimization
```

### Best Practices
1. **Be Specific**: Quantify requirements (≤2 seconds, 10+ users)
2. **Phase Realistically**: Break into 2-3 week phases
3. **Consider Dependencies**: List all external services needed
4. **Set Clear Boundaries**: Define what's out of scope

### Example: Auto-Graph Scope
```markdown
## One-line Summary
Web-based codebase analysis tool that generates hierarchical architectural graphs with AI agent detection for enterprise compliance.

## What We're Building
- **Input**: Local codebase path or file upload
- **Processing**: AST parsing, semantic analysis, graph construction
- **Output**: Interactive web visualization + multi-format export
- **Core Logic**: Hierarchical graph generation with agent detection

## Performance Requirements
- **Processing Speed**: ≤30 seconds for 100 files
- **Memory Usage**: ≤500MB for typical codebase
- **Web Response**: ≤2 seconds for graph display

## Development Phases
1. **Phase 1**: Core parsing and graph construction
2. **Phase 2**: Web interface and visualization
3. **Phase 3**: Agent detection and compliance features
```

## 🏗️ Template 3: STRUCTURE_MAP

### Purpose
Defines the technical architecture, file organization, and integration patterns for your project.

### When to Use
- **After SCOPE_DOC is complete**
- **Before any coding begins**
- **When you need to coordinate multiple AI agents**
- **When you need consistent code organization**

### Key Sections

#### Directory Layout
```markdown
## Directory Layout
```
my-project/
├── run_web.py                 # Main entry point
├── src/
│   ├── api/                   # API routes and endpoints
│   ├── services/              # Business logic and external services
│   ├── models/                # Data models and schemas
│   ├── utils/                 # Shared utilities and helpers
│   └── web/                   # Flask web application
├── tests/                     # Unit tests
├── static/                    # Static assets (CSS, JS, images)
├── templates/                 # HTML templates
└── data/                      # Data storage and cache
```

#### Layer Responsibilities
```markdown
## Layer Responsibilities
- **API**: Handle HTTP requests, validate input, return responses
- **Services**: Business logic, external API integration, data processing
- **Models**: Data structures, validation, database operations
- **Utils**: Shared functions, configuration, logging
- **Web**: Flask app setup, routing, template rendering
```

#### API Integration Rules
```markdown
## API Integration Rules
- **RESTful Design**: Use standard HTTP methods (GET, POST, PUT, DELETE)
- **JSON Responses**: All API responses in JSON format
- **Error Handling**: Consistent error response structure
- **Rate Limiting**: Implement basic rate limiting for external APIs
```

#### Cursor/Replit Constraints
```markdown
## Cursor/Replit Constraints
- **Cursor**: Backend logic, API development, database integration
- **Replit**: Frontend components, UI design, user experience
- **Integration**: Shared project structure and common knowledge docs
- **Communication**: Use intermediate JSON outputs for data exchange
```

### Best Practices
1. **Keep It Simple**: Avoid over-engineering the structure
2. **Be Consistent**: Use the same patterns throughout
3. **Consider Scalability**: Structure should support future growth
4. **Document Dependencies**: Clear integration points between layers

### Example: Auto-Graph Structure
```markdown
## Directory Layout
```
Auto-Graph/
├── run_web.py                 # Main entry point
├── src/
│   ├── parser/                # AST parsing and file analysis
│   ├── analyzer/              # Codebase analysis engine
│   ├── llm_integration/       # OpenAI integration with caching
│   ├── graph_builder/         # Hierarchical graph construction
│   ├── export/                # Multi-format export system
│   ├── web/                   # Flask web application
│   ├── agent_detection/       # AI agent usage detection
│   ├── observability/         # Audit and compliance features
│   └── utils/                 # Shared utilities
├── tests/                     # Unit tests
├── examples/                  # Sample codebases
└── graph/                     # Output directory
```

## 🧪 Template 4: REALITY_TESTS

### Purpose
Defines testing strategy, quality assurance framework, and expected behavior for all scenarios.

### When to Use
- **Before implementation begins**
- **When you need to ensure quality standards**
- **When stakeholders need confidence in the system**
- **When you need to prevent common failure modes**

### Key Sections

#### Sample Data Payloads
```markdown
## Sample Data Payloads
- **User Registration**: Email, password, preferences
- **Recommendation Request**: User ID, context, preferences
- **Data Export**: User ID, date range, format preference
- **Error Response**: Error code, message, suggested action
```

#### Critical User Flows
```markdown
## Critical User Flows
1. **Primary Flow**: User registration → Data input → Recommendation generation
2. **Error Flow**: Invalid input → Error message → Retry option
3. **Recovery Flow**: Service failure → Fallback response → Retry mechanism
4. **Export Flow**: Data selection → Format choice → Download file
```

#### Edge Cases
```markdown
## Edge Cases
- **Empty Input**: Handle gracefully, provide helpful error message
- **Large Data Sets**: Implement pagination and progress indicators
- **Network Failures**: Retry with exponential backoff
- **Invalid Formats**: Validate input and provide clear feedback
- **Rate Limiting**: Handle API limits gracefully
```

#### Performance Test Scenarios
```markdown
## Performance Test Scenarios
- **Small Dataset**: 100 records, <1 second processing
- **Medium Dataset**: 1000 records, <5 seconds processing
- **Large Dataset**: 10000 records, <30 seconds processing
- **Concurrent Users**: Support 5+ simultaneous users
- **Memory Usage**: <200MB for typical usage
```

#### Expected Behavior on Failure
```markdown
## Expected Behavior on Failure
- **API Failures**: Return cached data or fallback response
- **Database Errors**: Log error, return user-friendly message
- **Network Issues**: Retry automatically, show progress indicator
- **Invalid Input**: Clear error message with suggestions
- **System Overload**: Queue requests, show estimated wait time
```

### Best Practices
1. **Test Real Scenarios**: Use actual data and user flows
2. **Plan for Failure**: Define behavior for all error cases
3. **Set Performance Targets**: Quantify acceptable performance
4. **Consider User Experience**: How failures affect user perception

### Example: Auto-Graph Reality Tests
```markdown
## Sample Data Payloads
- **Calculator App**: 15 files, basic CRUD operations
- **Risk Platform**: 50+ files, complex business logic
- **AI-Enhanced App**: Codebase with OpenAI/LangChain integration

## Critical User Flows
1. **Primary Flow**: Upload codebase → Analysis → Graph visualization
2. **Error Flow**: Invalid file → Error message → Retry option
3. **Recovery Flow**: Large codebase → Progress tracking → Partial results
4. **Export Flow**: Graph generation → Format selection → Download

## Edge Cases
- **Empty Files**: Handle gracefully, skip with warning
- **Binary Files**: Detect and exclude from analysis
- **Circular Dependencies**: Identify and report
- **Large Codebases**: Implement timeout and memory limits
- **Network Failures**: Cache results, retry mechanisms
```

## 🤖 Template 5: AGENT_PROMPT_MAP

### Purpose
Provides specific prompts and communication patterns for each AI agent to ensure consistent, high-quality development.

### When to Use
- **During active development**
- **When coordinating multiple AI agents**
- **When you need consistent output quality**
- **When you want to optimize agent performance**

### Key Sections

#### ChatGPT Prompt Templates
```markdown
## ChatGPT Prompt Templates

### Project Scoping
"Help me scope out a [project type] with these requirements:
- [specific requirement 1]
- [specific requirement 2]
- [specific requirement 3]
- Stack: [technology stack]
- Performance: [performance requirements]

Focus on:
1. Core functionality breakdown
2. Technical architecture decisions
3. Potential challenges and solutions
4. User experience considerations
5. Implementation priorities"
```

#### Cursor Prompts
```markdown
## Cursor Prompts

### Backend Development
"Build the [module name] for [project name]:

Requirements:
- [specific requirement 1]
- [specific requirement 2]
- [specific requirement 3]

Follow the structure map:
- Create [directory path]
- Implement [specific functionality]
- Add error handling and logging
- Include unit tests

Use these constraints:
- Keep it simple and readable
- Add comprehensive error handling
- Follow the established project structure
- Include docstrings and type hints"
```

#### Replit Prompts
```markdown
## Replit Prompts

### Frontend Components
"Create a [component name] for [project name]:

Requirements:
- [specific requirement 1]
- [specific requirement 2]
- [specific requirement 3]

Constraints:
- HTML/CSS/JS only
- No external frameworks
- Mobile-friendly
- Fast loading

Focus on:
1. User experience
2. Visual feedback
3. Error handling
4. Responsive design"
```

#### Integration Prompts
```markdown
## Integration Prompts

### Component Integration
"Integrate the [component 1] with [component 2]:

Requirements:
- [integration requirement 1]
- [integration requirement 2]

Data Flow:
- [component 1] provides [data type] to [component 2]
- [component 2] processes [data type] and returns [result type]

Error Handling:
- Handle [specific error scenario]
- Provide fallback behavior
- Log errors appropriately"
```

### Best Practices
1. **Be Specific**: Include exact requirements and constraints
2. **Reference Structure**: Always mention the established project structure
3. **Set Quality Standards**: Include error handling and testing requirements
4. **Maintain Consistency**: Use similar prompt patterns across agents

### Example: Auto-Graph Agent Prompts
```markdown
## Cursor Prompts

### AST Parser Development
"Build the core parsing module for Auto-Graph:

Requirements:
- Parse Python files using AST
- Extract functions, classes, imports
- Handle parsing errors gracefully
- Generate symbol maps
- Support for multiple file types

Follow the structure map:
- Create src/parser/ directory
- Implement AST-based parsing
- Add error handling and logging
- Include unit tests

Use these constraints:
- Keep it simple and readable
- Add comprehensive error handling
- Follow the established project structure
- Include docstrings and type hints"

## Replit Prompts

### File Upload Interface
"Create a file upload interface for Auto-Graph:

Requirements:
- Drag-and-drop file upload
- Progress indicator
- File validation
- Simple, clean design

Constraints:
- HTML/CSS/JS only
- No external frameworks
- Mobile-friendly
- Fast loading

Focus on:
1. User experience
2. Visual feedback
3. Error handling
4. Responsive design"
```

## 🧠 Template 6: AGENTIC_LOGIC_GUIDE

### Purpose
Defines patterns and best practices for building intelligent systems with AI integration.

### When to Use
- **When your project includes AI features**
- **When you need to integrate external AI services**
- **When you want to ensure AI system reliability**
- **When you need to optimize AI performance and costs**

### Key Sections

#### Context Management Architecture
```markdown
## Context Management Architecture
- **State Preservation**: How to maintain conversation/context across requests
- **Context Cleanup**: When and how to clear old context to prevent bloat
- **Context Limits**: Maximum context size and management strategies
- **Context Security**: How sensitive data is handled and protected
- **Context Validation**: Ensuring context data is valid and safe
```

#### External Service Integration
```markdown
## External Service Integration
- **Service Management**: Centralized orchestration of all external services
- **Error Handling**: Retry mechanisms, circuit breakers, graceful degradation
- **Performance Optimization**: Response caching, request batching, rate limiting
- **Cost Management**: Monitoring and controlling API usage costs
```

#### Testing Intelligent Logic
```markdown
## Testing Intelligent Logic
- **Flow Testing**: Multi-step scenarios, context preservation, intent recognition
- **Performance Testing**: Concurrent users, large context, complex operations
- **Quality Assurance**: Response validation, safety checks, consistency testing
```

#### Implementation Guidelines
```markdown
## Implementation Guidelines
- **Code Organization**: Separation of concerns, modular design, configuration management
- **Best Practices**: Prompt engineering, response processing, context management
- **Common Patterns**: Service factory, response pipeline, context manager
```

### Best Practices
1. **Plan for Failure**: Design systems that work even when AI services fail
2. **Optimize Costs**: Implement caching and efficient usage patterns
3. **Ensure Safety**: Validate all AI responses and handle edge cases
4. **Monitor Performance**: Track usage, costs, and system behavior

### Example: Auto-Graph Agentic Logic
```markdown
## Context Management Architecture
- **State Preservation**: Cache LLM analysis results by file hash
- **Context Cleanup**: Clear cache when files change
- **Context Limits**: Maximum 2000 tokens per analysis request
- **Context Security**: No sensitive code content in prompts
- **Context Validation**: Validate file content before analysis

## External Service Integration
- **Service Management**: Centralized OpenAI client with caching
- **Error Handling**: Fallback to basic analysis when LLM fails
- **Performance Optimization**: Cache results to reduce API calls by 80%+
- **Cost Management**: Monitor API usage and implement rate limiting

## Testing Intelligent Logic
- **Flow Testing**: Test complete analysis pipeline with sample codebases
- **Performance Testing**: Verify processing time and memory usage
- **Quality Assurance**: Validate graph structure and agent detection accuracy
```

## 🚀 Using the Templates Together

### Step-by-Step Process

1. **Start with FOUNDATION_KNOWLEDGE**
   - Define your project's core values and constraints
   - Establish AI agent roles and responsibilities
   - Set clear boundaries for what you won't build

2. **Create SCOPE_DOC**
   - Define specific requirements and deliverables
   - Break down the project into phases
   - Set performance and quality targets

3. **Develop STRUCTURE_MAP**
   - Design the technical architecture
   - Define file organization and patterns
   - Establish integration rules

4. **Plan REALITY_TESTS**
   - Define testing strategy and scenarios
   - Plan for edge cases and failures
   - Set quality assurance standards

5. **Create AGENT_PROMPT_MAP**
   - Develop specific prompts for each AI agent
   - Ensure consistent communication patterns
   - Optimize for quality and efficiency

6. **Define AGENTIC_LOGIC_GUIDE**
   - Plan AI integration patterns
   - Design error handling and fallback strategies
   - Optimize for performance and cost

### Template Relationships

```
FOUNDATION_KNOWLEDGE
    ↓ (informs)
SCOPE_DOC
    ↓ (informs)
STRUCTURE_MAP
    ↓ (informs)
REALITY_TESTS
    ↓ (informs)
AGENT_PROMPT_MAP
    ↓ (informs)
AGENTIC_LOGIC_GUIDE
```

### Quality Checklist

- [ ] **FOUNDATION_KNOWLEDGE**: Clear constraints and agent roles defined
- [ ] **SCOPE_DOC**: Specific requirements and phases planned
- [ ] **STRUCTURE_MAP**: Technical architecture and patterns established
- [ ] **REALITY_TESTS**: Testing strategy and quality standards defined
- [ ] **AGENT_PROMPT_MAP**: Specific prompts for each agent created
- [ ] **AGENTIC_LOGIC_GUIDE**: AI integration patterns planned (if applicable)

## 🎯 Success Metrics

### Structural Integrity
- **Project Structure**: Maintains consistent file organization across all agents
- **Agent Boundaries**: Each agent stays within defined responsibilities
- **Integration Success**: Components connect without structural conflicts
- **Code Clarity**: Readable, maintainable code that doesn't confuse agents

### Development Efficiency
- **Planning Focus**: 60-70% of time spent on knowledge documents
- **Implementation Speed**: 1-2 days for core functionality
- **Debugging Strategy**: Terminal execution over excessive logging
- **Testing Approach**: Unit tests only after core functionality is complete

### Agent Coordination
- **Cursor Guidelines**: Follow established project structure, avoid structural changes
- **Replit Guidelines**: Create visual components independently, integrate cleanly
- **ChatGPT Guidelines**: Maintain project vision, avoid scope creep and debugging loops

## 📚 Resources

- **[WALKTHROUGH.md](WALKTHROUGH.md)** - Complete example using Auto-Graph
- **[AGENT_ORCHESTRATION.md](AGENT_ORCHESTRATION.md)** - AI agent coordination strategies
- **[COST_OPTIMIZATION.md](COST_OPTIMIZATION.md)** - Budget management techniques
- **[Auto-Graph Example](Auto-Graph/)** - Complete implementation reference

---

**Ready to transform your development process? Start with FOUNDATION_KNOWLEDGE and build your next AI-powered project with confidence!** 