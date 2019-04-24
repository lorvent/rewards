FORMAT: 1A

# Rewards

#  [/api]
# Group AuthController
status_code=0 - valid
status_code=1 - not valid

## Verify token [POST /api/verify_token]


+ Request (application/json)
    + Body

            {
                "token": "token"
            }

+ Response 200 (application/json)
    + Body

            {
                "valid": "valid_token",
                "status_code": 0
            }

+ Response 200 (application/json)
    + Body

            {
                "valid": "wrong_token",
                "status_code": 1
            }

## Add coins [POST /api/add_coins]


+ Request (application/json)
    + Body

            {
                "coins": "coins",
                "token": "token"
            }

+ Response 200 (application/json)
    + Body

            {
                "success": "success",
                "status_code": 0
            }

+ Response 400 (application/json)
    + Body

            {
                "error": "wrong_token",
                "status_code": 1
            }