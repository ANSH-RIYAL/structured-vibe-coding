# FOUNDATION_KNOWLEDGE

## Build Philosophy
- **Simplicity First**: Keep the stack minimal (Flask + HTML/CSS/JS)
- **Agent-Aware Focus**: Specifically designed for teams using AI agents
- **Performance Conscious**: Fast processing with intelligent caching
- **File Preservation**: Never modify original codebase, output to separate directory
- **User-Friendly**: Make complex codebases accessible to non-technical stakeholders

## AI Agent Roles & Division of Labor
- **Cursor Role:** Backend logic, AST parsing, LLM integration, graph construction, API development
- **Replit Role:** Frontend components, graph visualization, file upload UI, user interface design
- **ChatGPT Role:** Project scoping, semantic analysis prompts, business context extraction

## Development Rules & Constraints
- **Project Structure:** Fixed folder/file naming conventions that must be followed
- **Stack Limitations:** Flask backend, HTML/CSS/JS frontend, OpenAI API integration
- **Code Organization:** Separate concerns: parser, analyzer, graph_builder, export, web, agent_detection
- **Integration Patterns:** RESTful API communication between frontend and backend
- **AI Service Integration:** Centralized LLM client with caching and fallback mechanisms
- **Context Management:** State preservation for analysis sessions and progress tracking

## Data Realism Principles
- **Multi-language Support**: Python, JavaScript, Java, Go, Ruby, PHP, HTML, CSS, JSON, XML, YAML
- **AI Component Patterns**: Realistic detection of OpenAI, LangChain, Anthropic patterns
- **Graph Structure**: Hierarchical HLD/LLD organization with metadata
- **Export Formats**: JSON, YAML, CSV, DOT, HTML, Mermaid for different use cases
- **Performance Data**: Realistic file counts, processing times, and memory usage

## External Service Integration
- **Service Dependencies:** OpenAI API for LLM analysis, file system for codebase access
- **Integration Patterns:** Centralized LLM client with caching, error handling, and fallback
- **Error Handling:** Graceful degradation when external services fail
- **Performance Constraints:** Rate limiting, token limits, and response time optimization
- **Cost Management:** Caching strategies and API usage monitoring

## Quality Assurance Guidelines
- **Testing Strategy:** Unit tests for core components, integration tests for analysis pipeline
- **Error Handling:** Comprehensive error handling across all endpoints and services
- **Performance Requirements:** <30 seconds analysis time for typical codebases
- **User Experience:** Real-time progress tracking and interactive visualization
- **AI Service Reliability:** Fallback mechanisms and response validation

## What We're NOT Doing
- Real-time collaborative editing or live code analysis
- Advanced machine learning model training or custom AI model development
- Complex authentication or user management systems
- Real-time WebSocket communication for live updates
- Advanced database integration or persistent storage
- Mobile app development or native mobile interfaces
- Enterprise compliance reporting (SOC2, HIPAA, GDPR, etc.)

## Output Goals
- **Codebase Analysis**: Generate comprehensive hierarchical graphs with metadata
- **Multi-format Export**: Support 6 different export formats (JSON, YAML, CSV, DOT, HTML, Mermaid)
- **Agent Detection**: Identify AI component usage patterns in codebases
- **Web Interface**: Interactive visualization with file upload and progress tracking
- **Performance Standards**: Maintain <30 seconds analysis time and 90%+ accuracy 