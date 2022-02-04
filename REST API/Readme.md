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
All REST APIs in Unit4 is documented in **Swagger UI** in something called a **Web Api Server**. 
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

By filling in all mandatory parameters, you can test the API by pressing **Try it out**.
A popup will open, so that you can enter the username and password (the API-user defined in the User Masterfile).


# Access control to REST APIs

When giving external systems access to perform operations against the Unit4 database via the REST API, it is important to be clear about which accesses the various systems should have. Be restrictive with access, if an external system only needs to read data, then one should only give read access to the APIs.
On ERP7, we recommend that you create an API user per. external system, so that you can provide individual access per. system.

You can read about how to create an API-user and how to provide access to the REST API in Unit4 ERP below.

We recommend that you create an API-user for each external system that will integrate with Unit4 ERP.
Then you will have full control over what each system can access.

**NB:** At the time of writing this, it is not possible in ERPx to have more than one API-user.
This is because the API users in ERPx must authenticate with Unit4 IDS.

Create a API-user in Unit4 ERP as shown below, it is important to have checked the "Menu access" checkbox:
![image](https://user-images.githubusercontent.com/98328584/152523684-1449c3ec-c75b-4376-9f2a-f492cc71db2d.png)

Then you need to grant access to the roles and companies that is relevant to the API-user.
In the example below, the API-user has full access via the SYSTEM role, but it is recommended that you use a separate integration role if you want to restrict access.
![image](https://user-images.githubusercontent.com/98328584/152523929-0bbbe5c8-48fb-4299-b76a-d554be25089f.png)

On the last Security-tab, it is very important that the API-user is configured with a default logon company. 
If this is not defined then you will always get an "Unauthorized" error message when using the APIs.

In order for an API-user to access data via the REST API, you must grant access to both the Public API and the business object.
This is done in the **Public API Access** and **Object Access** screens.

First you grant access to the API itself. Here you provide access to relevant API users/roles and define whether the external system should have access to create, read, update or delete data (CRUD):
![image](https://user-images.githubusercontent.com/98328584/152527002-2cd33b55-6a7e-44a3-88e8-ca1cd2c4df25.png)

In addition, you must grant access to the actual business object used by the API. This is done via the Object Access screen.
These business objects are the same objects that are used for reporting in the Information Browser.
If the external system is only to have read access to data, then it is recommended to only check the checkbox for R / Read.
![image](https://user-images.githubusercontent.com/98328584/152527310-e9c6d7e9-896e-4bc4-8283-5117da54f1d9.png)

When access are granted, you must do an application recycle or run iisreset to clear the cache.
Alternatively, you can delete the cache via REST API calls from eg PostMan. This can only be done by an API-user with the SUPER role:
![image](https://user-images.githubusercontent.com/98328584/152527853-0c964230-e488-4578-adbd-aa5bf28f7e62.png)




# ODATA syntax
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








