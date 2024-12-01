# Data-Source-API-Analyst-Test

## Client Requirements
The client has requested the following features using GitHub's REST API:  
1. **Search Repositories**: Ability to search public repositories based on filters like programming language, number of stars, etc.  
2. **Get Commits**: Retrieve the commit history of repositories, including commit messages, authors, and dates.  
3. **Get Contents**: Fetch specific contents of repositories, such as README files or source code files.  

## Repository Structure
- **`README.md`**: Documents the assignment's purpose, methodology, and reflections.  
- **`/Content`**: Contains related files:  
  - API documentation.  
  - Python code for handling authentication, data extraction, error handling, rate limits, and pagination (if applicable).  
  - Troubleshooting guides and approaches to data cleaning.  
- **`/Postman_Collection`**: Includes Postman collections created to test GitHub API endpoints.  

## Approach
This project focuses on leveraging GitHub's REST API to fulfill client requirements. The implementation includes:  

### **API Research**
- Identified and tested the required GitHub API endpoints:  
  - **Repositories**: `/search/repositories     https://api.github.com/search/repositories?q=language:python`  
  - **Commits**: `/repos/{owner}/{repo}/commits     https://api.github.com/repos/django/django/commits`  
  - **Contents**: `/repos/{owner}/{repo}/contents/{path}      https://api.github.com/repos/django/django/contents/README.rst`  

- Studied GitHub API documentation to manage:  
  - **Requests Logic**: Properly structured GET requests with query parameters.  
  - **Pagination**: Extracting complete data using paginated requests.  
  - **Rate Limits**: Adhering to GitHub's limits to prevent blocking.  
  - **Error Handling**: Implemented strategies to handle authentication errors, invalid requests, etc.  

### **Implementation**
- **Postman**:  
  - Created a collection named `GitHub API Test` with requests for authentication, repository search, commits, and content retrieval.  
  - Defined environment variables for API tokens and headers to streamline requests.  
  - Tested each endpoint and saved responses for documentation.  

## Reflection
This section will include reflections on the assignment after completion. It will highlight the challenges faced, solutions implemented, and lessons learned throughout the process.  

## Troubleshooting
- **401 Unauthorized**: Ensured the access token is active, valid, and properly included in the request headers.  
- **403 Rate Limit Exceeded**: Implemented a retry mechanism after a specified wait time to respect rate limits.  
- **422 Unprocessable Entity**: Double-checked query parameters and request body structure to meet API specifications.  

## Next Steps
1. Export Postman collections as `.json` files and save them in the `/Postman_Collection` folder.  
2. Add the saved responses and documentation to the `/Content` folder.  
3. Submit the final repository.  
