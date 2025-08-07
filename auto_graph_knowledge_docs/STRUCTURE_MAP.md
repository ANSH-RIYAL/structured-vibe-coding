# STRUCTURE_MAP

## Directory Layout
```
Auto-Graph/
├── run_web.py                   # Main web application entry point
├── requirements.txt             # Python dependencies
├── setup.py                    # Package setup
├── .gitignore                  # Git ignore patterns
├── README.md                   # Project documentation
├── src/                        # Source code
│   ├── __init__.py
│   ├── main.py                 # CLI entry point
│   ├── parser/                 # AST parsing and symbol extraction
│   │   ├── __init__.py
│   │   ├── ast_parser.py       # Python AST parsing
│   │   └── file_parser.py      # Multi-file parsing
│   ├── analyzer/               # Codebase analysis and traversal
│   │   ├── __init__.py
│   │   └── codebase_analyzer.py # Main analysis coordinator
│   ├── llm_integration/        # LLM-powered semantic analysis
│   │   ├── __init__.py
│   │   ├── llm_client.py       # OpenAI API client
│   │   ├── relationship_mapper.py # Relationship mapping
│   │   └── semantic_analyzer.py # Semantic analysis
│   ├── graph_builder/          # Graph construction and management
│   │   ├── __init__.py
│   │   └── enhanced_graph_builder.py # Enhanced graph building
│   ├── export/                 # Multi-format export functionality
│   │   ├── __init__.py
│   │   └── enhanced_exporter.py # Enhanced export with metadata
│   ├── visualization/          # Graph visualization components
│   │   ├── __init__.py
│   │   └── graph_visualizer.py # Graph visualization
│   ├── agent_detection/        # AI component detection
│   │   ├── __init__.py
│   │   ├── agent_detector.py   # AI pattern detection
│   │   ├── context_extractor.py # Business context extraction
│   │   └── risk_assessor.py    # Risk assessment
│   ├── config/                 # Configuration management
│   │   ├── __init__.py
│   │   └── settings.py         # Application settings
│   ├── web/                    # Flask web application
│   │   ├── __init__.py
│   │   ├── flask_app.py        # Flask application
│   │   ├── static/             # Static assets
│   │   │   ├── css/
│   │   │   │   └── style.css
│   │   │   └── js/
│   │   │       └── app.js
│   │   └── templates/          # HTML templates
│   │       ├── index.html
│   │       └── graph_view.html
│   ├── models/                 # Data models and schemas
│   │   ├── __init__.py
│   │   ├── graph_models.py     # Graph data models
│   │   └── schemas.py          # Pydantic schemas
│   └── utils/                  # Utilities and helpers
│       ├── __init__.py
│       ├── file_utils.py       # File system utilities
│       └── logger.py           # Logging utilities
├── tests/                      # Test suite
│   ├── __init__.py
│   ├── test_agent_detection.py
│   ├── test_analyzer.py
│   ├── test_observability.py
│   ├── test_parser.py
│   └── test_semantic_analyzer.py
├── examples/                   # Sample codebases for testing
│   ├── sample_codebases/       # Example codebases
│   │   ├── calculator_app/     # Simple calculator app
│   │   ├── risk_compliance_platform/ # Fintech platform
│   │   └── ai_enhanced_app.zip
│   └── sample_graphs/          # Example graph outputs
│       ├── autograph_graph_*.json
│       └── example_ecommerce_graph.json
├── graph/                      # Output directory for generated graphs
├── logs/                       # Application logs
├── cache/                      # LLM response caching
└── knowledge_docs_templates/   # Knowledge documentation templates
    ├── AGENT_PROMPT_MAP_template.md
    ├── AGENTIC_LOGIC_GUIDE_template.md
    ├── FOUNDATION_KNOWLEDGE_template.md
    ├── REALITY_TESTS_template.md
    ├── SCOPE_DOC_template.md
    └── STRUCTURE_MAP_template.md
```

## Layer Responsibilities
- **/parser:** AST parsing, symbol extraction, multi-language support
- **/analyzer:** Main analysis coordination, pipeline orchestration
- **/llm_integration:** OpenAI API integration, semantic analysis, relationship mapping
- **/graph_builder:** Hierarchical graph construction, HLD/LLD organization
- **/export:** Multi-format export (JSON, YAML, CSV, DOT, HTML, Mermaid)
- **/visualization:** Graph visualization and rendering
- **/agent_detection:** AI component detection, pattern recognition, metadata enrichment
- **/web:** Flask web application, API endpoints, frontend integration
- **/models:** Data schemas, Pydantic models, graph structures
- **/utils:** File utilities, logging, configuration helpers

## API Integration Rules
- Use RESTful JSON endpoints (`/api/analysis/upload`, `/api/analysis/<id>/status`)
- Responses include `success`, `data`, `error` fields
- File upload via multipart/form-data
- Real-time progress updates via polling
- Export downloads via file streaming

## Static File Serving
- Serve frontend via root `/` with Flask templates
- Serve static assets from `/static` via Flask
- Cache static files for performance optimization
- Support for large file uploads and downloads

## Cursor/Replit Constraints
- **Cursor:** Backend logic, API implementation, data processing, LLM integration
- **Replit:** Frontend components, UI design, graph visualization, user interactions
- **ChatGPT:** Project scoping, documentation, prompt engineering, business analysis

## External Service Integration
- **Service Management:** Centralized LLM client with caching and fallback
- **Error Handling:** Graceful degradation when OpenAI API fails
- **Performance:** Rate limiting, token optimization, response caching
- **Fallback Strategies:** Offline analysis, cached responses, error recovery

## Project Setup Tips
- Environment configuration with OpenAI API key
- Development server setup with Flask
- Testing framework with pytest
- Deployment configuration for production

## Frontend Integration Entry Point
- Default frontend: `/src/web/templates/index.html`
- JavaScript entry: `/src/web/static/js/app.js`
- State management: Session-based analysis tracking
- Real-time updates: Polling-based progress tracking 