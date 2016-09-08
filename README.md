# Banking
Simple banking service that exposes a RESTful API

###Requirements
- Create a simple banking service that supports the following requests which are exposed over REST:

    - Create new account
    - Retrieve balance
    - Deposit funds
    - Widthdraw funds

- There should be no UI, we are just creating the service
- Use SoapUI as a means to invoke the REST services
- Use SoapUI to create success mock responses for all requests.
- Use Maven to build the project and pacakge it as a WAR.
- Use JBOSS to host the WAR

###Stack
- Java 8 (7 is OK)
- Maven
- Spring (for bean management / inversion of control)
- Jersey
- Jersey-Jackson
- SoapUI
- JBOSS


###Sample Requests and Responses

- Create account sample request:
```
POST /banking/createAccount
```
```
{
	"account":{
		"account-holder": "Jeb Bartlet",
		"DOB":"1940-08-03",
		"SIN":"123-456-789"
	}, 
	"account-type":"SAVINGS",
	"IDtypes":["PASSPORT", "CREDIT CARD"]
}
```
- Create Account Sample Response:
HTTP Response code 200
```
{"accountNumber":1234567890}
```

- Retrieve Balance Sample Request:

```
GET /banking/balance/{accountNumber}
```

- Retrieve Balance Sample Response:
```
{
"accountNumber":"1234567890",
"balance": "$550,000"
}
```

- Desposit Funds Request:
POST /banking/deposit/{accountNumber}

```
{"amount":"$6,500"}
```
- Desposit Funds Sample Response:

Response code 200. No response body.

- Withdraw Funds Sample Request:

POST /banking/withdraw/{accountNumber}

```
{"amount":"$25,000"}
```

- Withdraw Funds Sample Response:
```
{ 
"accountNumber":"1234567890",
"balance": "$550,000"
}
```
