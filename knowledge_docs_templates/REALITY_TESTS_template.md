# REALITY_TESTS

## Sample Data Payloads

### Request Example
```json
{
  "input_data": "example input",
  "context": {},
  "options": {}
}
```

### Response Example
```json
{
  "success": true,
  "data": {
    "result": "example output",
    "metadata": {}
  },
  "error": null
}
```

### Frontend Inputs
- Define the HTML form fields and their purposes
- Specify input validation requirements
- Define user interaction patterns

## Critical User Flows
- **Primary Flow:** Define the main user journey from start to finish
- **Error Flow:** Define how the system handles errors and failures
- **Recovery Flow:** Define how the system recovers from failures
- **Alternative Flows:** Define any secondary user journeys

## Edge Cases
- **Input Validation:** What happens with invalid or malformed inputs
- **Service Failures:** What happens when external services fail
- **Performance Limits:** What happens under high load or resource constraints
- **Data Corruption:** What happens when data is corrupted or incomplete
- **Network Issues:** What happens during network interruptions

## Performance Test Scenarios
- **Concurrent Users:** How many simultaneous users can be handled
- **Large Data Sets:** How the system handles large amounts of data
- **Complex Operations:** How the system handles resource-intensive operations
- **Memory Usage:** How the system manages memory under load
- **Response Times:** Expected latency for different operations

## Expected Behavior on Failure
- **Backend:**
  - HTTP status codes to return
  - Error message format and content
  - Logging and monitoring requirements
- **Frontend:**
  - How errors are displayed to users
  - Retry mechanisms and user guidance
  - Graceful degradation strategies

## Quality Assurance Requirements
- **Testing Strategy:** How to test the system functionality
- **Error Handling:** What error scenarios must be handled
- **Performance Monitoring:** How to track system performance
- **User Experience:** How to ensure good user experience during failures
- **Security:** How to protect against common security issues 