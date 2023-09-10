### API TESTING PROJECT
### Introduction

This is a API Testing project with an exploratory and educational purposes based on some of the endpoints stored in https://gorest.co.in/
Since we do no have a detailed documentation about some matters related to the behaviour of this API, this will be covered also in the content of this repository through exploration and experimentation in order to discover unknown information.

Information about the project: 
On the site I have seen that the dev team is still active, responding to questions made in the Help foro section.
The documentation that we have available is the one presented in the homepage of the gorest site.

### Table of content
------

- [Testing Strategy](#testing-strategy)
   - [Name of the project](#name-of-the-project)
   - [Objectives](#objectives)
   - [Test Approach](#test-approach)
   - [Test Environment](#test-environment)
   - [Test Scenarios](#test-scenarios)
   - [Test Execution](#test-execution)
   - [Defect Management](#defect-management)
   - [Reporting#](#reporting)
  

### TESTING STRATEGY

### Name of the project:

Go REST API Testing

### Objectives:

- Learn about how the API works. 
- Apply some learned knowledge.
- Practice and determine the test types to perform.
- Complete some specifications related to the API documentation.
- Report some issues as samples.

### Test Approach

- Over the API testing strategy, integration and some performance testing will be made.
- The parameters will be tested in order to determine among others things the type of data allowed and the required fields.
- Response messages check.
- Interoperability, check the integration among the different components.
- Error handling.
- Data.

### Test Environment

- Application Environment: QA Environment https://gorest.co.in/
- Tools: Postman and Newman.
- Test Data: Sample data sets for various scenarios (csv file in DDT folder).

### Test Scenarios

These are some examples of the test scenarios that can be performed for this API.

- Create a New User: 

    Send a POST request to create a new user.
    Verify that the user is created successfully and the response status code is 201 (Created).

- Get User Details:

    Send a GET request to retrieve user details for a specific user (e.g., user with ID 2963788).
    Verify that the user details are retrieved correctly, and the response status code is 200 (OK).

- Delete User:

    Send a DELETE request to delete a specific user (e.g., user with ID 2968563).
    Verify that the user is deleted successfully, and the response status code is 204 (No Content).

- Retrieve Posts:
  
     Send a GET request to retrieve a list of posts.
     Verify that the posts are retrieved correctly, and the response status code is 200 (OK).

- Retrieve Post Comments:
     Send a GET request to retrieve comments associated with a specific post (e.g., post with ID 2963).
     Verify that the post's comments are retrieved correctly, and the response status code is 200 (OK).

- Get User Details for Non-Existent User:

     Send a GET request to retrieve user details for a user ID that does not exist.
     Verify that the API returns a response with a 404 status code.

- Update User Details with Invalid Data:

     Send a PUT or PATCH request to update user details with invalid data (e.g., invalid email format).
     Verify that the API returns an appropriate error response (e.g., 422 Unprocessable Entity).

- Retrieve Non-Existent Post:

     Send a GET request to retrieve a post that does not exist (e.g., post with ID 999999).
     Verify that the API returns a response with a 404 status code.

### Test Execution 

- Execute test scripts using Postman and Newman.
- Document results, including success and failure cases.

### Defect Management
- Use Github Issues for the management of issues.
- Document defects with detailed steps to reproduce.
    
### Reporting
- Generate comprehensive test reports after each test (html-extra newman reporter).
