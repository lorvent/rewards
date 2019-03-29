FORMAT: 1A

# Rewards

#  [/api]
# Group AuthController

## login user [PUT /api/login]


+ Request (application/json)
    + Body

            {
                "email": "email@email.com",
                "password": "password"
            }

+ Response 200 (application/json)
    + Body

            {
                "access_token": "jwt_token",
                "token_type": "bearer",
                "expires_in": "15420",
                "user": {
                    "id": "1",
                    "email": "email@email.com"
                }
            }

## user info [GET /api/me]


+ Response 200 (application/json)
    + Body

            [
                {
                    "id": "1",
                    "email": "email@email.com"
                }
            ]

## Log the user out (Invalidate the token). [GET /api/logout]


+ Response 200 (application/json)
    + Body

            {
                "message": "Successfully logged out"
            }

## Refresh a token. [GET /api/refresh]


+ Response 200 (application/json)
    + Body

            {
                "access_token": "jwt_token",
                "token_type": "bearer",
                "expires_in": "15420",
                "user": {
                    "id": "1",
                    "email": "email@email.com"
                }
            }

## Verify token [GET /api/verify_token]


+ Request (application/json)
    + Body

            {
                "token": "token"
            }

+ Response 200 (application/json)
    + Body

            {
                "valid": "not_valid"
            }

+ Response 200 (application/json)
    + Body

            {
                "valid": "valid"
            }

## Add coins [POST /api/add_coins]


+ Request (application/json)
    + Body

            {
                "token": "token"
            }

+ Response 200 (application/json)
    + Body

            {
                "success": "success"
            }

+ Response 400 (application/json)
    + Body

            {
                "error": "wrong_token"
            }