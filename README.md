# Next.js CRUD Operations with Token Refresh

This TypeScript code provides a comprehensive utility for performing CRUD (Create, Read, Update, Delete) operations in a Next.js application while managing token-based authentication. The code includes a mechanism to automatically refresh the access token when it expires.

## Dependencies

- **next/navigation**: Utilized for routing within Next.js applications.

## Interfaces

### `Location`

Represents the origin of the API.

### `ErrorResponse`

Defines the structure of an error response from the server, including a message, status, and optional error data.

### `RequestOptions`

Specifies options for making HTTP requests, including method, headers, and body.

### `CrudOptions`

Extends `RequestOptions` and introduces an `action` property to denote CRUD operations.

### `RefreshTokenResponse`

Represents the response format when refreshing the access token.

## Functions

### `refreshAccessToken`

An asynchronous function responsible for refreshing the access token by sending a POST request to the designated endpoint. It handles errors gracefully and returns the new access token if successful.

**Example:**

```typescript
const newAccessToken = await refreshAccessToken();
if (newAccessToken) {
    console.log('Access token refreshed successfully:', newAccessToken.accessToken);
} else {
    console.log('Failed to refresh access token.');
}
