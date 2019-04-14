
## Laravel JWT 

Laravel JWT Authentication tutorial:

- laravel new project-name
- composer require tymon/jwt-auth:dev-develop --prefer-source


## For Testting

# Create a user account for testing

Endpoint : 127.0.0.1:8000/api/register
Method: POST
Payload:

name: Name
email: email@email.com
password: secret
password_confirmation: secret

# User login
Endpoint : 127.0.0.1:8000/api/login
Method: POST
Payload:

email: email@email.com
password: secret

# Accessing an unprotected route

Endpoint : 127.0.0.1:8000/api/open
Method: GET

# Access a protected endpoint

Endpoint : 127.0.0.1:8000/api/open
Method: GET
Payload:

Authorization: Bearer insert_user_token_here

# Get the authenticated user data

Endpoint : 127.0.0.1:8000/api/user
Method: GET
Payload:

Authorization: Bearer insert_user_token_here

# Use invalid token to access a users data

Endpoint : 127.0.0.1:8000/api/user
Method: GET
Payload:

Authorization: Bearer wrongtoken

# Accessing a protected route without a token

Endpoint : 127.0.0.1:8000/api/closed
Method: GET

