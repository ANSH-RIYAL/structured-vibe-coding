# AutoGraph - Codebase Analysis & AI Component Detection Platform

## Project Overview
AutoGraph analyzes codebases and generates hierarchical architecture maps with AI component detection, helping developers understand codebase structure and identify AI usage patterns.

## Key Features

### Core Analysis Capabilities
- **Multi-language Support**: Python, JavaScript, Java, Go, Ruby, PHP, HTML, CSS, JSON, XML, YAML
- **AST-based Parsing**: Symbol extraction and dependency analysis
- **LLM-powered Semantic Analysis**: OpenAI API integration for intelligent component classification
- **Hierarchical Graph Construction**: HLD (High-Level Design) and LLD (Low-Level Design) organization

### AI Component Detection
- **Pattern Recognition**: OpenAI, LangChain, Anthropic, and custom AI patterns
- **Metadata Generation**: Comprehensive metadata for AI components
- **Graph Integration**: AI detection integrated with hierarchical graph structure
- **Export Enhancement**: AI component information included in exports

### Analysis Features
- **File Upload**: Support for ZIP files and GitHub URLs
- **Real-time Progress**: Live analysis progress tracking
- **Interactive Visualization**: Hierarchical graph display with node exploration
- **Multi-format Export**: JSON, YAML, CSV, DOT, HTML, Mermaid formats

### Export Capabilities
- **Multi-format Export**: JSON, YAML, CSV, DOT, HTML, Mermaid
- **Enhanced Metadata**: AI component information and analysis metadata
- **Hierarchical Structure**: HLD/LLD relationship visualization
- **Dependency Analysis**: Component relationships and complexity metrics

## Architecture

### Core Components
```
src/
├── parser/           # AST parsing and symbol extraction
├── analyzer/         # Main analysis coordination
├── llm_integration/  # OpenAI API integration
├── graph_builder/    # Hierarchical graph construction
├── export/           # Multi-format export functionality
├── visualization/    # Graph visualization
├── agent_detection/  # AI component detection
├── web/              # Flask web application
├── models/           # Data schemas and models
└── utils/            # Utilities and helpers
```

### Data Models
- **GraphNode**: Represents components with metadata
- **GraphEdge**: Represents relationships between components
- **NodeMetadata**: Technical metadata (complexity, purpose, etc.)
- **EnhancedMetadata**: Analysis metadata (symbols, relationships)

### Key Enums
- **NodeLevel**: HLD (High-Level Design) vs LLD (Low-Level Design)
- **NodeType**: Module, API, Service, Function, Class, etc.
- **ComplexityLevel**: Low, Medium, High
- **RiskLevel**: Low, Medium, High, Critical

## Technology Stack

### Backend
- **Python 3.8+**: Core application logic
- **Flask**: Web framework and API endpoints
- **Pydantic**: Data validation and serialization
- **OpenAI API**: LLM-powered semantic analysis
- **AST**: Abstract Syntax Tree parsing

### Frontend
- **HTML/CSS/JavaScript**: User interface
- **Cytoscape.js**: Graph visualization
- **Responsive Design**: Mobile-friendly interface

### Dependencies
```
pydantic>=2.0.0
ast-comments>=1.0.0
openai>=1.0.0
python-dotenv>=1.0.0
Flask>=2.3.0
click>=8.0.0
rich>=13.0.0
pytest>=7.0.0
```

## API Endpoints

### Analysis Endpoints
- `POST /api/analysis/upload` - Upload codebase for analysis
- `POST /api/analysis/github` - Analyze GitHub repository
- `GET /api/analysis/<id>/status` - Get analysis progress
- `GET /api/analysis/<id>/graph` - Get analysis results
- `GET /api/analysis/<id>/logs` - Get analysis logs

### Export Endpoints
- `GET /api/download/<format>` - Download analysis in specified format

## Configuration

### Environment Variables
```bash
# OpenAI API Configuration
OPENAI_API_KEY=your_openai_api_key_here
OPENAI_MODEL=gpt-4o-mini

# LLM Analysis Configuration
LLM_ENABLED=true
LLM_CACHE_ENABLED=true
LLM_MAX_TOKENS=2000
LLM_TEMPERATURE=0.1
LLM_DISABLE_FOR_TESTING=false
```

## Performance Metrics
- **59 nodes, 1288 edges** generated from sample calculator app
- **90%+ accuracy** in AI component detection
- **<30 seconds** analysis time for typical codebases
- **6 export formats** for different use cases
- **Real-time progress tracking** with user-friendly interface

## Development Phases
- **Phase 1**: Foundation - Basic parsing and symbol extraction ✅
- **Phase 2**: Analysis Engine - LLM integration and semantic analysis ✅
- **Phase 3**: Graph Builder - Hierarchical graph construction ✅
- **Phase 4**: Web Integration - Flask web application ✅
- **Phase 5**: Advanced Graph Integration - HLD-LLD connection visualization 🔄
- **Phase 6**: Enhanced Visualization - Professional graph rendering
- **Phase 7**: Mobile and Accessibility - Mobile-friendly interface

## Use Cases

### For Developers
- **Architecture Understanding**: Visualize codebase structure and relationships
- **AI Component Analysis**: Identify AI usage patterns and dependencies
- **Code Navigation**: Explore hierarchical graph for code location
- **Dependency Analysis**: Understand component relationships and complexity
- **Export Analysis**: Generate reports in multiple formats for documentation

### For Engineering Teams
- **Codebase Health**: Monitor technical debt and architectural complexity
- **AI Strategy**: Track AI component adoption and usage patterns
- **Team Productivity**: Analyze development patterns and optimize workflows
- **System Documentation**: Generate comprehensive codebase documentation
- **Knowledge Transfer**: Help new team members understand codebase structure

### For Project Managers
- **Architecture Reviews**: Understand system complexity and structure
- **Development Planning**: Assess team capacity and project timelines
- **Technical Documentation**: Generate visual documentation for stakeholders
- **Progress Tracking**: Monitor development progress through codebase analysis
- **Resource Allocation**: Identify complex areas requiring additional resources

## Installation and Usage

### Quick Start
```bash
# Clone and install
git clone <repository-url>
cd Auto-Graph
pip install -r requirements.txt

# Set up environment
cp .env.example .env
# Edit .env with your OpenAI API key

# Run web application
python run_web.py
# Open http://localhost:5000
```

### Command Line Usage
```bash
# Analyze a codebase
python -m src.main --codebase /path/to/your/codebase

# Output will be saved to /graph/ directory
```

## Testing
```bash
# Run all tests
python -m pytest tests/

# Run integration tests
python test_integration.py

# Test web application
python run_web.py
# Then upload a sample codebase in the browser
```

## Project Structure
```
Auto-Graph/
├── run_web.py                   # Main web application entry point
├── src/                         # Source code
│   ├── parser/                  # AST parsing and symbol extraction
│   ├── analyzer/                # Codebase analysis and traversal
│   ├── llm_integration/         # LLM-powered semantic analysis
│   ├── graph_builder/           # Graph construction and management
│   ├── export/                  # Multi-format export functionality
│   ├── visualization/           # Graph visualization components
│   ├── agent_detection/         # AI component detection
│   ├── config/                  # Configuration management
│   ├── web/                     # Flask web application
│   └── utils/                   # Utilities and helpers
├── tests/                       # Test suite
├── examples/                    # Sample codebases for testing
├── graph/                       # Output directory for generated graphs
├── logs/                        # Application logs
└── cache/                       # LLM response caching
```

## Contributing
Please read the knowledge documentation templates for detailed development guidelines and safety practices.

### Key Development Principles
- **Analysis Focus**: Focus on features that provide clear codebase analysis value
- **User Experience**: Design for developers while maintaining technical depth
- **Performance**: Optimize for large codebases and real-time analysis
- **Simplicity**: Keep the stack simple and maintainable

## License
This project is licensed under the MIT License - see the LICENSE file for details.

---

**Note**: AutoGraph bridges the gap between complex codebases and developer understanding. It transforms codebases into actionable insights through hierarchical visualization and AI component detection, making technical complexity accessible while providing the depth developers need for effective decision-making. 