# Azure OpenAI APIM Policies

This repository encompasses a set of APIM (Azure API Management) policies aimed at enhancing various aspects of API management, including:

1. **Load Balancing:** Ensuring efficient distribution of traffic across multiple backend services.
2. **Keyless Authentication:** Authentication mechanisms that don't rely on API keys for access.
3. **Model Validation and API Versioning:** Validate the model name  the API version.
3. **Retry with exponential backoff:** Retry logic based on response status codes and conditional routing of requests 
3. **Priority Management Based on Subscription Keys:** Controlling access and resources based on subscription priority.
4. **Event Hub Logging:** Logging events for monitoring and analytics.

## Scope and Structure

### Policy Scopes
These policies are implemented at both the product and API levels, catering to specific functionalities:
- **API-Level Policies:** Encompass Load Balancing, retry mechanism, madel name validation and Keyless Authentication for specific APIs.
- **Product-Level Policies:** Comprise Priority Management based on subscription keys and Event Hub logging to manage product access and log essential events.
### Products Defined
- **Chatbot:** Assigned a high-priority status due to the expectation of a high request volume per minute.
- **BatchProcessor:** Identified as a low-priority product with a lower request per minute (RPM) count.

