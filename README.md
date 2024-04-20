# My Assignment

## API Routes

- `/api/auth/register`

  - Method: POST
  - Description: Register a new user with email and password.
  - Request Body:
    ```json
    {
      "email": "example@example.com",
      "password": "password123"
    }
    ```
  - Response:
    ```json
    {
      "message": "An OTP has been sent to your inbox"
    }
    ```
  - Example:
    ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/c162f479-d97c-4ba1-ac86-27ca088dc2f8)
  

- `/api/users/login`

  - Method: POST
  - Description: Login with email and password to generate JWT token.
  - Request Body:
    ```json
    {
      "email": "example@example.com",
      "password": "password123"
    }
    ```
  - Response:
    ```json
    {
      "message": "Login successful"
    }
    ```
  - Cookies:

    ```bash
    "your-jwt-token"
    ```

  - Example:
    ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/daf55b25-ab39-49e4-b76b-471b8c2f0d66)

- `/api/auth/verify`

  - Method: POST
  - Description: Verify user's email using OTP.
  - Request Body:
    ```json
    {
      "email": "example@example.com",
      "otp": "123456"
    }
    ```
  - Response:
    ```json
    {
      "message": "Email verified successfully."
    }
    ```
  - Example
    ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/365ea83b-8acd-4e46-a487-0695270ace73)

- `/api/users/generate-otp`

  - Method: POST
  - Description: Resend OTP to user's email for verification.
  - Query Params:
    ```json
    {
      "email": "example@example.com"
    }
    ```
  - Response:
    ```json
    {
      "message": "An OTP has been sent to your inbox"
    }
    ```
  - Example:
    ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/85e91652-9c3a-4c76-92c3-8c1d08900c6d)
   
- `/api/user/get-user-details`

  - Method: GET
  - Description: Retrieve user information using JWT token.
  - Headers:
    ```
    Authorization: Bearer <jwt_token>
    ```
  - Response:

    ```json
    {
      "_id": "662186deff922bf782a8d070",
      "email": "mail@example.com",
      "__verified": true,
      "createdAt": "2024-04-18T20:47:26.619Z",
      "updatedAt": "2024-04-18T21:02:31.218Z",
      "__v": 0
    }
    ```

    - Example:

      ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/a69a1a20-2b01-4939-97a0-2608e77caa76)

- `/api/user/fill-user-details`

  - Method: POST
  - Description: Add extra information like location, age, and work details to user profile.
  - Headers:
    ```
    Authorization: Bearer <jwt_token>
    ```
  - Request Body:
    ```json
    {
      "location": "New York",
      "age": "30",
      "work": "Software Engineer"
    }
    ```
  - Response:

    ```json
    {
      "message": "User details updated successfully."
    }
    ```

    -Example:

    ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/d91278f1-dd5d-4ccb-bb36-319628edecda)

## MongoDB Schema

- User Schema:

  ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/a1a36a6d-3f03-4bba-a6b4-03497f8c1684)

- OTP Schema

  ![image](https://github.com/ritikjee/monter-backend-assignment/assets/96499245/339b7b6b-2763-4571-ace6-f1f23ee3e296)

