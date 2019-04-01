FORMAT: 1A

# Rewards

#  [/api]
# Group AuthController

## Verify token [POST /api/verify_token]


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
                "coins": "coins",
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