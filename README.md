### API TESTING PROJECT
### Introduction

Welcome! This project is designed for exploration and educational purposes, focusing on endpoints provided by https://gorest.co.in/.
Since I don't have access to detailed documentation about certain aspects of this API's behavior, I'll be experimenting within this repository. This approach will allow me to uncover unknown information through hands-on exploration.

On the site I have seen that the dev team is still active, responding to questions made in the Help foro section.
The documentation that we have available is the one presented in the homepage of the gorest site.

You can get your own access token by login here https://gorest.co.in/consumer/login

### Table of content
------
- [Testing Strategy Overview](#testing-strategy-overview)
   - [Name of the project](#name-of-the-project)
   - [Objectives](#objectives)
   - [Scope](#scope)
   - [Test Environment](#test-environment)
   - [Tools](#tools)
   - [Test Data](#test-data)
   - [Test Scenarios](#test-scenarios)
   - [Test Execution](#test-execution)
   - [Defect Management](#defect-management)
   - [Reporting](#reporting)
  

### TESTING STRATEGY OVERVIEW

### Name of the project

Go REST API Testing
<br>

### Objectives
- Learn about how the API works. 
- Identify and practice various test types.
- Complete specifications related to the API documentation.
- Examine parameters to assess data types, allowed values, and required fields.
- Verify response messages for correctness.
- Evaluate the integration among different components.
- Assess how the API handles errors.
- Provide sample issue reports.
- Check requests response time.

### Scope
- The API endpoints needed to address the objectives:
 <br>

| USER  | Description |                              
| --- | --- |
|GET /public/v2/users/  |                 Retrieves the list of all the users |
|GET, DELETE, PUT /public/v2/users/{id} |  Retrieves user details, Deletes user and Edits user details |
|POST /public/v2/users/     |             Creates a new user|

This part also includes the searching of the user by email, gender, status and name.
<br>
<br>

| POST | Description | 
| --- | --- |
|GET /public/v2/posts/             |     Retrieves the list of all the posts |
|GET /public/v2/posts/{post_id}    |      Retrieves the post by its id|
|POST /public/v2/users/{id}/posts/ |       Creates a new post for the user|
|DELETE /public/v2/posts/{id}  |          Deletes a post |
|PATCH  /public/v2/posts/{id} |            Modifies post detail/s |
<br>

|COMMENT| Description |
| --- | --- |
|GET /public/v2/comments/ |               Retrieves the list of all the comments |
|GET /public/v2/comments/{id} |            Retrieves comment by its id |
|POST /public/v2/posts/{id}/comments/ |    Creates a new comment for a specific post |
|DELETE /public/v2/comments/{id}       |  Deletes a comment by its id |
<br>

|TO-DO| Description |
| --- | --- |
|GET /public/v2/todos/  |                 Retrieves the list of all the to dos|
|GET /public/v2/todos/{id}|               Retrieves a to-do resource by its id |
|POST /public/v2/users/{id}/todos|        Creates a to-do for a user|
|DELETE /public/v2/todos/{id}     |       Deletes a to-do by its id |
<br>

- Functional Testing, to ensure that the API behaves correctly according to its specification, business logic or general expectations.

- Peformance Testing, aspects related to response times.

- Dependencies: The system restores all the data every 24hs.

- OUT-OF-SCOPE: Database testing, UI/UX testing, Security Testing, OPTIONS and HEAD HTTP methods.
 <br>

### Test Level 

- Integration testing, to ensure integrated components work together correctly and data flows between them as expected.

### Test types

- Functional Testing, Test Automation, API Testing, Exploratory Testing.

### Test Environment
- Application Environment: QA Environment https://gorest.co.in/

### Tools 
- Postman and Newman.

  
### Test Data
- Sample data sets for various scenarios (csv file in DDT folder).
<br>

### Test Scenarios

These are some examples of the test scenarios that can be performed for this API.

- Create a New User: 

    1. Send a POST request to create a new user.
    2. Verify that the user is created successfully and the response status code is 201 (Created).

- Get User Details:

    1. Send a GET request to retrieve user details for a specific user (e.g., user with ID 2963788).
    2. Verify that the user details are retrieved correctly, and the response status code is 200 (OK).

- Delete User:

    1. Send a DELETE request to delete a specific user (e.g., user with ID 2968563).
    2. Verify that the user is deleted successfully, and the response status code is 204 (No Content).

- Retrieve Posts:
  
    1. Send a GET request to retrieve a list of posts.
    2. Verify that the posts are retrieved correctly, and the response status code is 200 (OK).

- Retrieve Post Comments:
  
    1. Send a GET request to retrieve comments associated with a specific post (e.g., post with ID 2963).
    2. Verify that the post's comments are retrieved correctly, and the response status code is 200 (OK).

- Get User Details for Non-Existent User:

    1. Send a GET request to retrieve user details for a user ID that does not exist.
    2. Verify that the API returns a response with a 404 status code.

- Update User Details with Invalid Data:

    1. Send a PUT or PATCH request to update user details with invalid data (e.g., invalid email format).
    2. Verify that the API returns an appropriate error response (e.g., 422 Unprocessable Entity).

- Retrieve Non-Existent Post:

    1. Send a GET request to retrieve a post that does not exist (e.g., post with ID 999999).
    2. Verify that the API returns a response with a 404 status code.
<br>

### Test Execution 

- Execute test scripts using Postman and Newman.
- Document results, including success and failure cases.

### Defect Management
- Use Github Issues for the management of issues.
- Document defects with detailed steps to reproduce.
    
### Reporting
- Generate comprehensive test reports after each test (html-extra newman reporter).
