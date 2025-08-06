# AGENT_PROMPT_MAP

## ChatGPT Prompt Templates
- "Help me define the phases for a tool that [description]"
- "Convert this user story into a SCOPE_DOC Phase plan"
- "Generate realistic JSON payload for a [feature]"
- "Design integration patterns for [specific functionality]"
- "Create testing strategies for [system component]"

## Cursor Prompts

### Backend Development
- "Add a new route in `/routes` for receiving this form submission"
- "Implement logic in `/services` to process [X]"
- "Update app.py to include new endpoint and service"
- "Create external service integration in `/services/`"
- "Implement error handling for [specific scenario]"

### Core Logic Implementation
- "Create a [specific component] that handles [functionality]"
- "Implement [business logic] with proper error handling"
- "Build [data processing] with validation and sanitization"
- "Add [feature] with appropriate logging and monitoring"
- "Create [integration] with fallback mechanisms"

### API Development
- "Create REST API endpoints for [functionality]"
- "Implement request/response validation for [endpoint]"
- "Add error handling and status codes for [API]"
- "Create documentation for [API endpoint]"
- "Implement rate limiting for [service]"

## Replit Prompts

### Frontend Components
- "Create a clean HTML form to upload [X]"
- "Generate `script.js` to make a `fetch()` call to `/api/submit`"
- "Build a table UI that displays this JSON result"
- "Create a responsive interface for [functionality]"
- "Build real-time status indicators for [service]"

### User Interface
- "Design a user-friendly interface for [feature]"
- "Create loading states for [operation]"
- "Build error display for [failure scenario]"
- "Implement responsive design for [component]"
- "Add accessibility features for [interface]"

### Integration
- "Connect frontend form to backend API"
- "Implement real-time updates for [feature]"
- "Create user feedback mechanisms"
- "Build progress indicators for [operation]"
- "Add retry mechanisms for failed operations"

## Integration Prompts

### Backend-Frontend Integration
- "Wire up `index.html` form to backend route `/api/submit` using JS"
- "Ensure error message from API is displayed under form in red"
- "Connect frontend state to backend data"
- "Implement real-time synchronization between frontend and backend"

### Data Flow Integration
- "Connect [component] to [service] with proper error handling"
- "Integrate [feature] with [external service]"
- "Link [frontend component] to [backend logic]"
- "Create data validation between [components]"

### Error Handling Integration
- "Implement comprehensive error handling across all endpoints"
- "Add validation for [input type]"
- "Create fallback mechanisms for [failure scenario]"
- "Ensure graceful degradation when [component] fails"

## Override Flags
- `#COMMERCIAL_FEATURE` → allow use of libraries or CSS frameworks
- `#ALLOW_AUTH` → enable session logic or login forms
- `#IGNORE_STRUCTURE_CONSTRAINTS` → allow folder creation (use sparingly)
- `#COMPLEX_INTEGRATION` → allow advanced external service integration
- `#REAL_TIME_FEATURES` → enable WebSocket or complex real-time updates
- `#ENTERPRISE_FEATURES` → enable advanced features and compliance

## Specific Implementation Prompts

### For Backend Services
```
"Implement [service name] that:
1. Handles [specific functionality]
2. Integrates with [external service]
3. Provides proper error handling
4. Includes logging and monitoring
5. Follows the established patterns in /services/
Use the existing structure and maintain consistency."
```

### For Frontend Components
```
"Build a [component type] that:
1. Accepts [input type] from users
2. Displays [output type] clearly
3. Handles errors gracefully
4. Provides good user feedback
5. Integrates with backend APIs
Use modern HTML/CSS/JS and maintain responsive design."
```

### For Integration
```
"Connect [component A] to [component B] by:
1. Establishing proper data flow
2. Implementing error handling
3. Adding validation where needed
4. Ensuring good user experience
5. Following established patterns
Maintain simplicity and avoid over-engineering."
``` 