DELOITTE CUSTOMER API

Extend Deloitte Customer API to Mobile Applications, Saas applications, systems and services with the Anypoint Deloitte Customers connector from Deloitte. 
The Deloitte Customer API gives a consumer the power to integrate Mobile Applications used by Customer Service Representatives to retrieve and update the customer details and maintain a copy of customers details.
With the MuleSoft Anypoint connector, consumers can create instant API connectivity to the Deloitte Customer API, providing a simple, pre-packaged way to manage customers data with Deloitte without having to connect with the back-end platform directly. 
URL
/customers
/customers/{customerID}
Method:
It defines the basic following operations for customers and uses data type and example fragments.
GET | POST | DELETE | PUT
URL Params
Required: Applicable for PUT & DELETE Methods.
customerID=[integer]
Optional: Not Applicable
Data Params
POST Request: 
The request message should not have a customer ID, as this is a system generated unique identifier and will be given by Deloitte customer system after successful addition and validation.
 

POST Success Response:
 

PUT Request: 
The relevant customer ID needs to be included in URI param per below  to perform update on particular customer details.

 
PUT Success Response:
 

DELETE Request:
The relevant customer ID needs to be included in URI param per below to perform delete on particular customer details.
 

DELETE Success Response:
 
HTTP Error Codes	
Code: 404 
Resource Name: customerdetails
Error Response:

 
Code: 415 Unsupported Media Type
Content Type: Text
 
 
Code: 405 Method Not Allowed
URL: Resource without Customer ID
 

Code: 400 Bad Request 
Body Content: Invalid JSON Format.
 
 


