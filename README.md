# CashCard
CashCard service for Family Cash Cards

```
Request:
  URI: /api/v1/cashcards/{id}
  Method: GET
  Body: None

Response:
  HTTP Status:
    200 OK if the user is authorized and the Cash Card was successfully retrieved
    403 UNAUTHORIZED if the user is unauthenticated or unauthorized
    404 NOT FOUND if the user is authenticated and authorized but the Cash Card cannot be found
  Response Body Type: JSON
  Example Response Body:
    {
      "id": 99,
      "amount": 123.45
    }

---
Request:
  URI: /api/v1/cashcards/
  Method: POST
  Body:
    {
      "amount": 123.45
    }

Response:
  HTTP Status:
    Status Code: 201 CREATED
    Header: Location=/cashcards/42

```