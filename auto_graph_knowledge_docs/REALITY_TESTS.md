# REALITY_TESTS

## Sample Data Payloads

### Request Example - Codebase Upload
```json
{
  "file": "multipart/form-data",
  "codebase_type": "zip",
  "analysis_options": {
    "include_ai_detection": true,
    "export_formats": ["json", "html", "mermaid"]
  }
}
```

### Response Example - Analysis Status
```json
{
  "success": true,
  "data": {
    "analysis_id": "analysis_12345",
    "status": "in_progress",
    "progress": 65,
    "stage": "graph_construction",
    "estimated_completion": "2024-01-15T10:30:00Z"
  },
  "error": null
}
```

### Response Example - Analysis Results
```json
{
  "success": true,
  "data": {
    "analysis_id": "analysis_12345",
    "status": "completed",
    "graph": {
      "metadata": {
        "codebase_path": "/path/to/codebase",
        "file_count": 150,
        "total_lines": 25000,
        "languages": ["python", "javascript"],
        "analysis_timestamp": "2024-01-15T10:25:00Z"
      },
      "nodes": [
        {
          "id": "node_1",
          "name": "API Layer",
          "type": "API",
          "level": "HLD",
          "metadata": {
            "purpose": "REST API endpoints",
            "complexity": "medium",
            "agent_touched": true,
            "agent_types": ["openai"],
            "risk_level": "medium"
          }
        }
      ],
      "edges": [
        {
          "from_node": "node_1",
          "to_node": "node_2",
          "type": "depends_on",
          "metadata": {}
        }
      ]
    },
    "statistics": {
      "total_nodes": 59,
      "hld_nodes": 12,
      "lld_nodes": 47,
      "total_edges": 1288,
      "ai_components": 8,
      "high_risk_components": 3
    }
  },
  "error": null
}
```

### Frontend Inputs
- **File Upload Form**: Accept ZIP files and GitHub URLs with validation
- **Analysis Options**: Checkboxes for AI detection and export formats
- **Export Format Selection**: Multi-select for export formats (JSON, YAML, CSV, DOT, HTML, Mermaid)
- **Progress Tracking**: Real-time progress indicators and status updates
- **Graph Interaction**: Node selection, filtering, and exploration controls

## Critical User Flows
- **Primary Flow:** Upload codebase → Analysis progress → View results → Export reports
- **Error Flow:** Failed upload → Error display → Retry mechanism → Success
- **Recovery Flow:** Analysis failure → Fallback analysis → Partial results → User notification
- **Alternative Flows:** GitHub URL analysis, batch processing, AI detection only

## Edge Cases
- **Input Validation:** Invalid file formats, corrupted archives, empty codebases
- **Service Failures:** OpenAI API unavailable, rate limit exceeded, network timeouts
- **Performance Limits:** Very large codebases (>100MB), complex dependency graphs
- **Data Corruption:** Malformed analysis results, incomplete graph data
- **Network Issues:** Interrupted uploads, connection timeouts, partial downloads

## Performance Test Scenarios
- **Concurrent Users:** 10 simultaneous analysis sessions
- **Large Data Sets:** 500+ files, 50,000+ lines of code
- **Complex Operations:** Multi-language codebases with deep dependencies
- **Memory Usage:** Efficient handling of large AST trees and graph structures
- **Response Times:** <30 seconds for typical codebases, <5 seconds for status updates

## Expected Behavior on Failure
- **Backend:**
  - HTTP 400 for invalid uploads, 500 for analysis failures
  - Detailed error messages with retry suggestions
  - Graceful degradation to basic analysis when LLM fails
  - Comprehensive logging for debugging
- **Frontend:**
  - Clear error messages with actionable guidance
  - Retry mechanisms for failed operations
  - Progress indicators for long-running operations
  - Graceful handling of network interruptions

## Quality Assurance Requirements
- **Testing Strategy:** Unit tests for core components, integration tests for analysis pipeline
- **Error Handling:** Comprehensive error scenarios for all API endpoints
- **Performance Monitoring:** Response time tracking and resource usage monitoring
- **User Experience:** Intuitive interface for codebase analysis
- **Security:** File upload validation, content scanning, secure data handling 