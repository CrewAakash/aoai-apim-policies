# Azure OpenAI APIM Policies

The repository includes a collection of Azure API Management (APIM) policy samples aiming for improving interactions with Azure OpenAI Service.

These samples focus on providing a head start for implementing key aspects as mentioned below.

1. **Load Balancing:** Ensuring efficient round robin based distribution of traffic across multiple backend services.
2. **Keyless Authentication:** Authentication mechanisms that don't rely on AOAI  keys for access.
3. **Request Validation and API Versioning:** Validate the model name  the API version.
3. **Retry with exponential backoff:** Retry logic based on response status codes and conditional routing of requests 
3. **Priority Management Based on Subscription Keys and Quota Allocation:** Controlling access and resources allocation based on subscription priority.
4. **Event Hub Logging:** Logging events for monitoring and analytics.
5. **Circuit Breaker:** Temporarily halting subsequent requests upon error.
5. **Adaptive Token Rate Limiting:** Adjusts the distribution of tokens based on the current demand of each consumer.

## Scope and Structure

### Policy Scopes
These policies are implemented at both the product and API levels, catering to specific functionalities:
- **API-Level Policies:** Encompass Load Balancing, retry mechanism, madel name validation and Keyless Authentication for specific APIs.
- **Product-Level Policies:** Comprise Priority Management based on subscription keys and Event Hub logging to manage product access and log essential events.
### Products Defined
- **Chatbot:** Assigned a high-priority status due to the expectation of a high request volume per minute.
- **BatchProcessor:** Identified as a low-priority product with a lower request per minute (RPM) count.
- **SimpleCircuitBreaker:** Demonstrates a simple circuit breaker pattern.
- **AdaptiveRateLimit:** Demonstrates a dynamic rate limiting strategy that adjusts token distribution from a global token bucket based on the varying demand of the consumers.