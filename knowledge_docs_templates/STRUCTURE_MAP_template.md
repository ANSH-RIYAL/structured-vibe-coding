# STRUCTURE_MAP

## Directory Layout
```
/
├── backend/
│   ├── app.py
│   ├── routes/
│   ├── services/
│   └── models/
├── frontend/
│   ├── index.html
│   ├── styles.css
│   └── script.js
├── static/
├── config/
├── tests/
└── [additional_directories]
```

## Layer Responsibilities
- **/routes:** Define API routes only, no logic
- **/services:** Business logic, processing, external service integration
- **/models:** Data schemas and helpers
- **/frontend:** User-facing code (HTML/CSS/JS)
- **/static:** JSON files, images, etc.
- **/config:** App settings and environment parsing
- **/[additional]:** Define purpose of any additional directories

## API Integration Rules
- Use only JSON endpoints
- Follow naming conventions (`/api/submit`, `/api/status`)
- Responses must include `success`, `data`, `error` fields
- Define how external services are integrated

## Static File Serving
- Serve frontend via root `/`
- Serve static data from `/static` via Flask/FastAPI
- Define caching strategy for performance

## Cursor/Replit Constraints
- No folder name changes once initialized
- Replit generates entire components from scratch
- Cursor integrates, stitches, and extends only via documented layers
- Define specific constraints for each agent

## External Service Integration
- **Service Management:** How external services are coordinated
- **Error Handling:** What happens when external services fail
- **Performance:** How to handle rate limits and costs
- **Fallback Strategies:** Alternative approaches when services are unavailable

## Project Setup Tips
- Environment configuration requirements
- Development server setup
- Testing framework setup
- Deployment configuration

## Frontend Integration Entry Point
- Default frontend file location
- JavaScript logic entry point
- State management approach
- Real-time update requirements 