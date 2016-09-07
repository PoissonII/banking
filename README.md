# Banking
Simple banking service that exposes a RESTful API

###Requirements
Create a simple banking service that supports the following requests which are exposed over REST:

- Create new account
- Retrieve balance
- Deposit funds
- Widthdraw funds
- Transfer funds to existing account

###Stack
- Java 8 (7 is OK)
- Maven
- Spring (for bean management / inversion of control)
- Jersey
- Jersey-Jackson
- SoapUI

###Sample Requests and Responses

- Create account sample request:
POST /banking/createAccount
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
- Create account sample response:
HTTP Response code 200
```
{"accountNumber":1234567890}
```

- Retrieve Balance Request:

GET /banking/balance/{accountID}

- Retrieve Balance Response:
```
{"balance": "$550,000"}
```
