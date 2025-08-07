# AGENT_PROMPT_MAP

## ChatGPT Prompt Templates
- "Help me define the phases for a codebase analysis tool that generates hierarchical graphs"
- "Convert this user story into a SCOPE_DOC Phase plan for AutoGraph"
- "Generate realistic JSON payload for a codebase analysis response"
- "Design integration patterns for OpenAI API with caching and fallback"
- "Create testing strategies for AI component detection and graph generation"

## Cursor Prompts

### Backend Development
- "Add a new route in `/src/web/flask_app.py` for receiving codebase uploads"
- "Implement logic in `/src/analyzer/codebase_analyzer.py` to coordinate the analysis pipeline"
- "Update `/src/llm_integration/llm_client.py` to include OpenAI API integration with caching"
- "Create AI component detection in `/src/agent_detection/agent_detector.py`"
- "Implement multi-format export in `/src/export/enhanced_exporter.py`"

### Core Logic Implementation
- "Create a FileParser that handles multi-language codebase parsing with AST analysis"
- "Implement LLMClient with proper error handling and fallback mechanisms"
- "Build EnhancedGraphBuilder with hierarchical HLD/LLD graph construction"
- "Add AI component detection with pattern recognition"
- "Create multi-format export functionality with JSON, YAML, CSV, DOT, HTML, Mermaid"

### API Development
- "Create REST API endpoints for codebase analysis and status tracking"
- "Implement request/response validation for file uploads and analysis requests"
- "Add error handling and status codes for analysis pipeline failures"
- "Create documentation for API endpoints with example requests/responses"
- "Implement rate limiting for OpenAI API calls and cost management"

### Data Models
- "Create Pydantic schemas for GraphNode, GraphEdge, and metadata structures"
- "Implement hierarchical graph models with HLD/LLD organization"
- "Build metadata models for AI component detection and analysis"
- "Design export format models for multi-format graph representation"
- "Create analysis session models for tracking progress"

## Replit Prompts

### Frontend Components
- "Create a clean HTML form to upload codebase ZIP files and GitHub URLs"
- "Generate `app.js` to make fetch calls to `/api/analysis/upload` and `/api/analysis/<id>/status`"
- "Build an interactive graph visualization using Cytoscape.js for hierarchical graphs"
- "Create a responsive interface for displaying analysis progress and results"
- "Build real-time status indicators for analysis pipeline stages"

### User Interface
- "Design a user-friendly interface for codebase upload and analysis tracking"
- "Create loading states for analysis pipeline with progress indicators"
- "Build error display for failed uploads and analysis errors"
- "Implement responsive design for graph visualization and analysis results"
- "Add accessibility features for graph interaction and exploration"

### Graph Visualization
- "Connect frontend graph visualization to backend analysis results"
- "Implement real-time updates for analysis progress and completion"
- "Create user feedback mechanisms for graph interaction and exploration"
- "Build progress indicators for multi-stage analysis pipeline"
- "Add retry mechanisms for failed analysis operations"

## Integration Prompts

### Backend-Frontend Integration
- "Wire up `index.html` form to backend route `/api/analysis/upload` using JavaScript"
- "Ensure error messages from API are displayed under form in red with retry options"
- "Connect frontend graph visualization to backend analysis results"
- "Implement real-time synchronization between frontend progress and backend analysis"

### Data Flow Integration
- "Connect FileParser to CodebaseAnalyzer with proper error handling"
- "Integrate LLMClient with semantic analysis and relationship mapping"
- "Link frontend graph visualization to backend graph data structures"
- "Create data validation between upload interface and analysis pipeline"

### Error Handling Integration
- "Implement comprehensive error handling across all analysis pipeline stages"
- "Add validation for file uploads and codebase formats"
- "Create fallback mechanisms for OpenAI API failures"
- "Ensure graceful degradation when analysis components fail"

## Override Flags
- `#ALLOW_AUTH` → enable session management for analysis tracking
- `#IGNORE_STRUCTURE_CONSTRAINTS` → allow folder creation for new components
- `#COMPLEX_INTEGRATION` → allow advanced OpenAI API integration patterns
- `#REAL_TIME_FEATURES` → enable progress tracking and real-time updates
- `#AI_DETECTION_FEATURES` → enable advanced AI component detection

## Specific Implementation Prompts

### For Backend Services
```
"Implement [service name] that:
1. Handles [specific functionality] for codebase analysis
2. Integrates with OpenAI API for semantic analysis
3. Provides proper error handling and fallback mechanisms
4. Includes logging and monitoring for analysis tracking
5. Follows the established patterns in /src/[module]/
Use the existing structure and maintain consistency with analysis requirements."
```

### For Frontend Components
```
"Build a [component type] that:
1. Accepts codebase uploads and displays analysis progress
2. Shows hierarchical graphs with AI component detection
3. Handles errors gracefully with user-friendly messages
4. Provides good user feedback for analysis results
5. Integrates with backend analysis APIs
Use modern HTML/CSS/JS and maintain responsive design for analysis users."
```

### For AI Integration
```
"Connect [component A] to [component B] by:
1. Establishing proper data flow for AI analysis
2. Implementing error handling for API failures
3. Adding validation for AI component detection
4. Ensuring good user experience during analysis
5. Following established patterns for codebase analysis
Maintain simplicity and avoid over-engineering while supporting analysis requirements."
```

### For Graph Generation
```
"Implement graph generation that:
1. Creates hierarchical HLD/LLD graph structure
2. Detects AI components and patterns in code
3. Generates metadata for nodes and edges
4. Provides multi-format export capabilities
5. Follows established patterns for graph construction
Ensure all features support codebase analysis and visualization requirements."
``` 