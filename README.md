## API Collection README

This Postman collection contains tests for a series of API endpoints related to user registration and authentication.

### How to Use

#### Run Tests Locally:

1. **Install Postman:**
   - Make sure you have Postman installed on your machine. You can download it from [here](https://www.postman.com/downloads/).

2. **Import Collection:**
   - Download the JSON file for this collection (e.g., "Regression_Suite_API").
   - Open Postman and click on the "Import" button in the top left corner.
   - Select the downloaded JSON file to import the collection into Postman.

3. **Set Environment Variables:**
   - Ensure that you have environment variables set for `email` and `password`. These variables will be used in the requests.
   - Update the environment variables with your test email and password.

4. **Run Tests:**
   - Open the imported collection in Postman.
   - Run the requests one by one or run the entire collection.
   - Monitor the test results in the "Tests" tab of each request.

#### Run Tests with GitHub Actions:

You can also execute the tests using GitHub Actions. The workflow is triggered automatically on every push to the main branch, or you can trigger it manually from the GitHub Actions UI.

### Collection Overview

#### Register - Successful
- **Method:** POST
- **URL:** https://reqres.in/api/register
- **Purpose:** Registers a user with the provided email and password.
- **Tests:**
  - Verifies that the response properties and values match the API documentation.
  - Checks the data type of each response property.
  - Validates that the response status code is 200 (OK).

#### Get User Registered
- **Method:** GET
- **URL:** https://reqres.in/api/users/4
- **Purpose:** Retrieves information about a registered user.
- **Tests:**
  - Verifies that the response contains the ID and email of the previously registered user.
  - Validates that the response status code is 200 (OK).

#### Login - Successful
- **Method:** POST
- **URL:** https://reqres.in/api/login
- **Purpose:** Logs in a user with the provided email and password.
- **Tests:**
  - Verifies that the response contains the token previously registered.
  - Validates that the response status code is 200 (OK).

### Authorization
The collection uses API key authentication. The API key is included in the collection variables.

### Environment Variables
- `idRetrieved`: Holds the ID of the registered user.
- `tokenRetrieved`: Holds the token retrieved after successful registration.

### API Reference
For more details about the API, please refer to the [ReqRes API documentation](https://reqres.in/).

