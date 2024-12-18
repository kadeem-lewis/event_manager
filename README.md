# User Management API

---

## Resolved Issues

### [Email Validation](https://github.com/kadeem-lewis/event_manager/issues/12)

- Added regex patterns to validate email formats and prevent invalid submissions.
- Implemented tests to cover various email edge cases, ensuring the validation logic handles both common and uncommon scenarios.

---

### [Password Validation](https://github.com/kadeem-lewis/event_manager/issues/10)

- Enforced password validation rules requiring:
  - A minimum length.
  - At least one special character.
  - At least one uppercase letter.
- Wrote tests to validate the handling of both valid and invalid passwords, covering edge cases.

---

### [Missing Access Tokens](https://github.com/kadeem-lewis/event_manager/issues/8)

- Created pytest fixtures to generate access tokens for:
  - Users.
  - Admins.
  - Managers.
- These fixtures ensure that all relevant tests requiring authentication pass successfully and streamline the testing process.

---

### [User Files Cleanup](https://github.com/kadeem-lewis/event_manager/issues/14)

- Resolved errors and warnings in related files to improve code quality and maintainability:
  - Removed a duplicate login route and function.
  - Eliminated unused imports and reorganized remaining imports for better readability.
  - Fixed duplicate field issues in `userListResponse`.
  - Added improved error handling for edge cases.
  - Addressed duplicate names in two tests to prevent conflicts.

---

### [Validation Error for login request](https://github.com/kadeem-lewis/event_manager/issues/5)

- Added the `email` field to the `login_request_data` fixture, resolving issues with pytest.
- Ensured the updated fixture aligns with the API's requirements and added tests to confirm its effectiveness.


### [User ID Validation](https://github.com/kadeem-lewis/event_manager/issues/3)

- Updated the `conftest` fixture to provide a UUID value for the `id` field.
- Resolved the issue where `test_user_response_valid` was failing because the `UserResponse` schema only accepts UUIDs.
- Ensured the pytest fixture aligns with the required data structure.

---

### [User Fixtures Missing Required Data](https://github.com/kadeem-lewis/event_manager/issues/1)

- Updated pytest fixtures to fix broken tests in `test_user_schemas.py`. These updates resolved three failing tests.
- Added missing fields:
  - `nickname` field to the base user fixture.
  - `first_name` field to the user update data.

### [Build and Publish to Dockerhub](https://github.com/kadeem-lewis/event_manager/issues/16)

- **Changed DockerHub Repository:** Updated the DockerHub image location to point to a personal profile and repository for better accessibility and management.
- **Added Email Service Environments:** Integrated email service environment variables into pytest for the GitHub Action workflow.
- **Package Updates:** Updated project dependencies to resolve vulnerabilities and maintain security and stability.
- **Build and Publish:** Configured GitHub Actions to build and publish the Docker image automatically to DockerHub upon successful tests.

---

## Testing and Coverage

Comprehensive testing was performed using pytest to ensure a high degree of confidence in the application:
- Achieved 90%+ test coverage.
- Added edge case tests for email and password validation.
- Verified all API endpoints requiring authentication using newly created fixtures.

---

## Deployment

**DockerHub Image Link:** ![Dockerhub deployment screenshot](./screenshots/Screenshot%202024-11-17%20at%2022-58-00%20ksl29_event_manager%20general.png)




## Learning Reflection

Through completing this project, I have learned a few new things about the product lifecycle and building production-ready applications. Some key takeaways include:

- Test at every step. This was a lesson that was emphasized early on but this project helped highlight just how important it was. By running pytest after every change, I was able to catch bugs early and ensure that the code was working as expected. I was able to easily identify broken areas of the application just be looking at the test results and seeing why particular tests failed. This made it much easier to debug and fix issues.

- Having a proper linter setup is crucial. By having a linter setup, I was able to get immediate feedback of this parts of the app had issues that needed to be fixed as soon as I opened a file. This helped me catch errors that I didn't notice from the UI or from the tests. This allowed me to feel more confident in the code I was writing and that it was following best practices.

- Thoroughly read the documentation. During the completion of this project, I watched the instructor video multiple times and also read the readme multiple times, this allowed me to understand the requirements of the project and what was expected of me. This helped me to ensure that I was on the right track and that I was completing the project as expected.