## Troubleshooting Guide

### 1. Error 401 Unauthorized
- **Cause**: The authentication token is incorrect or missing.
- **Solution**:
  - Check your token in Postman.
  - Ensure that the token is active and has the correct permissions for access.

### 2. Error 403 Rate Limit Exceeded
- **Cause**: The GitHub API request limit has been exceeded.
- **Solution**:
  - Use `X-RateLimit-Remaining` to track the remaining requests.
  - Reduce the frequency of requests or wait for the rate limit to reset.
