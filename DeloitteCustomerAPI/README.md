**DELOITTE CUSTOMER API**
----
 Extend Deloitte Customer API to Mobile Applications, Saas applications, systems and services with the Anypoint Deloitte Customer connector from Deloitte. 
 
The Deloitte Customer API gives a consumer the power to integrate Mobile Applications used by Customer Service Representatives to retrieve and update the customer details and maintain a copy of customers details.

With the MuleSoft Anypoint connector, consumers can create instant API connectivity to the Deloitte Customer API, providing a simple, pre-packaged way to manage customers data with Deloitte without having to connect with the back-end platform directly. 


* **URL**

  /customers
  
  /customers/{customerID}


* **Method:**
  
  It defines the basic following operations for customers and uses data type and example fragments.

  `GET` | `POST` | `DELETE` | `PUT`
  
*  **URL Params**

      **Required:** Applicable to PUT & DELETE Methods.
 
   `     customerID=[integer]`

      **Optional:** Not Applicable.
 
*  **Query Params**

      **Required:** Not Applicable.         

      **Optional:** Applicable to GET Method.

   `     customerID=[integer]`
   
            
* **Data Params**

   **POST Request:** 
      The request message should not have a customer ID, as Customer ID is a system generated unique identifier and will be given by Deloitte    customers management system after successful addition and data verification.
  
  ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/POST_Request.png)

    **POST Success Response:**
  
  ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/POST_Response.PNG)

    **PUT Request:** 
   The relevant customer ID needs to be included in URI param per below  to perform update on particular customer details.
   
   ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/PUT_Request.PNG)
 
    **PUT Success Response:** 
 
   ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/PUT_Response.PNG)
   
    **DELETE Request:** 
    The relevant customer ID needs to be included in URI param per below to perform delete on particular customer details.
    
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/DELETE_Request.png)
    
    **DELETE Success Response:** 
 
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/DELETE_Response.png)
 
 
* **HTTP Success Codes**

   **Code: 200**      
     
   * **LIST Content:** <br />     
       { "CustomerID" : 1, "FirstName" : "John", "LastName" : "Nelson", "Address" : { "AddressLine1" : "Unit No 18-22", "AddressLine2" : "Beresford Road", "Suburb" : "Seven Hills", "State" : "NSW" } }, { "CustomerID" : 2, "FirstName" : "David", "LastName" : "Tupper", "Address" : { "AddressLine1" : "Unit No 1-4", "AddressLine2" : "The Crescent", "Suburb" : "North Sydney", "State" : "NSW" } }                              
   * **PUT Content:** <br />  
       {"message": "Customer updated (but not really)"}
       
   * **DELETE Content:** <br />  
       {"message": "Customer details deleted(but not really)"}               
     
   **Code: 201** 
    
     Content: {"message": "Customer details added (but not really)"}
   

* **HTTP Error Codes**
  
   **Code: 404** 
   
     Resource Name: customerdetails
     
     **Error Response:**
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/http_404.png) 
    
   **Code: 415** 
   
     Content Type: Text
     
     **Error Response:**     
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/http_415_1.png) 
    
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/http_415_2.png)    

   **Code: 405** 
   
     URL Content: Resource without Customer ID
     
     **Error Response:**
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/http_405.png) 
    
   **Code: 400** 
   
     Body Content: Invalid JSON Format
     
     **Error Response:**     
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/http_400_1.png) 
    
    ![alt text](https://github.com/prakashr3/IntegrationHub/blob/master/DeloitteCustomerAPI/Images/http_400_2.png)
    
       
  
