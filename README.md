# CRUD Operations with Token Refresh in Next.js

This TypeScript code defines a set of utility functions for performing CRUD (Create, Read, Update, Delete) operations with token-based authentication in a Next.js application. The code includes functionality to refresh the access token if it has expired.

## Dependencies

- **next/navigation**: Used for routing in Next.js applications.
  
## Interfaces

- **Location**: Represents the origin of the API.
- **ErrorResponse**: Defines the structure of an error response from the server.
- **RequestOptions**: Specifies options for making HTTP requests.
- **CrudOptions**: Extends RequestOptions and includes an additional 'action' property for CRUD operations.
- **RefreshTokenResponse**: Represents the response when refreshing the access token.

## Functions

### `refreshAccessToken`

- Asynchronous function to refresh the access token by sending a request to the server.

### `performCrudOperation`

- Asynchronous function for executing CRUD operations.
- Merges default options with provided options and adds authentication headers.
- Handles token expiration by attempting to refresh the access token.

### CRUD Functions

- `performPost`: Performs a POST request.
- `performGet`: Performs a GET request.
- `performPut`: Performs a PUT request.
- `performDelete`: Performs a DELETE request.

## Usage

```typescript
import { performPost, performGet, performPut, performDelete } from 'path-to-file';

// Example usage
const postData = { /* your data */ };
const createResponse = await performPost('/api/resource', postData);
const readResponse = await performGet('/api/resource');
const updateResponse = await performPut('/api/resource/1', postData);
const deleteResponse = await performDelete('/api/resource/1');
