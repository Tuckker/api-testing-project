API Testing Project – End-to-End User Lifecycle Validation

This project demonstrates a structured and automated approach to API testing by validating the full user lifecycle (authentication, creation, update, and deletion) using Postman.

A collection of API requests was designed to simulate real-world usage scenarios, beginning with an authentication (login) request. The authentication workflow dynamically extracts an access token from the response and persists it as an environment variable, enabling secure and reusable authorization across subsequent requests using Bearer Token authentication.

To ensure consistency and traceability, pre-request scripting is implemented to generate dynamic timestamps, which are stored as environment variables and reused during execution. This reflects a practical approach to handling time-sensitive data in distributed systems.

The workflow continues with a user creation request, where response validation logic ensures that returned data adheres to the expected JSON schema. Critical data (such as user ID) is programmatically extracted and stored, enabling seamless chaining of dependent requests without manual intervention.

Subsequent requests include:
- Updating user data to validate PUT/PATCH operations and data mutation accuracy
- Deleting the user to validate cleanup operations and confirm correct API behavior via status code verification (204 No Content)

The entire workflow is parameterized using environment variables (e.g., base URL, authentication token, dynamic values), ensuring flexibility across environments and promoting reusability.

Additionally, both manual and collection runner executions are supported, enabling repeatable test runs and providing a foundation for integration into automated pipelines (e.g., CI/CD with Newman).

Key Capabilities Demonstrated:
- End-to-end API workflow validation (CRUD operations)
- Dynamic data handling using environment variables
- Automated response validation using JavaScript test scripts
- Token-based authentication management (Bearer Token)
- Pre-request and post-response scripting for state management
- Scalable test design aligned with real-world API usage patterns

This project reflects a strong understanding of API testing principles, test automation, and the ability to design maintainable and production-relevant test workflows.