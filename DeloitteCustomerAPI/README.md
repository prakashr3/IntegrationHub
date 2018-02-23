**DELOITTE CUSTOMER API**
----
 Extend Deloitte Customer API to Mobile Applications, Saas applications, systems and services with the Anypoint Deloitte Customers connector from Deloitte. 
 
The Deloitte Customer API gives a consumer the power to integrate Mobile Applications used by Customer Service Representatives to retrieve and update the customer details and maintain a copy of customers details.

With the MuleSoft Anypoint connector, consumers can create instant API connectivity to the Deloitte Customer API, providing a simple, pre-packaged way to manage customers data with Deloitte without having to connect with the back-end platform directly. 


* **URL**

  /customers
  
  /customers/{customerID}


* **Method:**
  
  It defines the basic following operations for customers and uses data type and example fragments.

  `GET` | `POST` | `DELETE` | `PUT`
  
*  **URL Params**

   <_If URL params exist, specify them in accordance with name mentioned in URL section. Separate into optional and required. Document data constraints._> 

   **Required: Applicable for PUT & DELETE Methods.**
 
   `customerID=[integer]`

   **Optional: Not Applicable**
 
   
* **Data Params**

  **POST Request:** 
    The request message should not have a customer ID, as this is a system generated unique identifier and will be given by Deloitte    customer system after successful addition and validation.
  
  ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/POST_Request.png)

 **POST Success Response:**
  
  <_What should the status c1ode be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** `{ id : 12 }`
 
* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**

  <_Just a sample call to your endpoint in a runnable format ($.ajax call or a curl request) - this makes life easier and more predictable._> 

* **Notes:**

  <_This is where all uncertainties, commentary, discussion etc. can go. I recommend timestamping and identifying oneself when leaving comments here._> 
