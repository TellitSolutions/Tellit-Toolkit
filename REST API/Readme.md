# Howto's for Unit4 REST APIs

This folder contains examples on how to use the Unit4 REST APIs.
We have choosen to share the examples as JSON-files that you could import into PostMan, and run them directly in your customer environement.
NB: You will need to change the URL of the examples to your customer specific URL for the webapi-server. You also need to have an ERP user with access to the APIs.

# Introduction to REST APIs

REST = “Representational State Transfer”.

REST has a client-server architecture that is based on a request / response design.
REST APIs communicate via HTTP / HTTPS, and make a "request" to perform database operations such as create, read, update and delete (CRUD)
![CRUD operations](https://user-images.githubusercontent.com/98328584/152490172-dac30aca-22b5-4f3c-b964-172f75ee86d0.png)

The request is made via a URL, and the structure of this URL is shown below:
![REST-URL](https://user-images.githubusercontent.com/98328584/152490044-38b0a5c5-d24f-4bef-b9a2-ca3ed00aedc8.png)

The return value from a request to a REST API is called a response.

# Swagger UI
All REST APIs in Unit4 is documented in Swagger UI in something called a Web Api Server. 
The URL to your webapi-server can be obtained from your system administrator.

If you are running Unit4 ERP on-premise, then Web Api Server must be published and Swagger UI must be activated by the system administrator in the Management Console.
Swagger UI is published by ticking the checkboxes marked in yellow below:
![image](https://user-images.githubusercontent.com/98328584/152490316-e50a6285-4466-406a-9c13-f8222ef6511d.png)

When Web Api Server is published and Swagger UI activated, you will be able to see documentation on all REST APIs,
and test these via the Swagger UI as shown below:
![image](https://user-images.githubusercontent.com/98328584/152490487-49928715-b737-40d7-83be-3a3a4c7ffb9f.png)

You can see details about each method and an overview of mandatory parameters and expected return value, by clicking on each method.
An example of this can be seen below:
![SwaggerTest](https://user-images.githubusercontent.com/98328584/152490752-357cd986-d565-45fb-979e-443bd016d0c6.png)


# ODATA
Unit4s REST APIs are using ODATA syntax to retrieve data. 
You can find some useful information on ODATA in this link: https://docs.microsoft.com/en-us/dynamics-nav/using-filter-expressions-in-odata-uris

There are a lot of operators and functions you can use to filter data through and REST API.
Below you can see an overview:
![REST operators and functions](https://user-images.githubusercontent.com/98328584/150995913-1943cbad-801a-4862-bace-f741f750d865.png)


# Additional sources of information
You can find more helpful sources of information on the links below:

https://www.odata.org/documentation/odata-version-2-0/uri-conventions/ 

https://docs.microsoft.com/en-us/dynamics-nav/using-filter-expressions-in-odata-uris

https://www.odata.org/getting-started/

https://www.odata.org/documentation/odata-version-2-0/uri-conventions/







