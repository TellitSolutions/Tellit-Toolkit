# Wanda Question

Wanda Question is a new way of communicating with the end user in Unit4 ERP.
Wanda Question is available as an action type in Extension Kit.

This example is a simple showcase on how you could ask the end user a question, and act on the true/false response.
The example contains of a Postman collection who kicks off the Webhook-trigger in Extension Kit, and the flow itself.

Below you can see an example of the dialogue between the end user and Wanda in Teams.
![Wanda communication](https://user-images.githubusercontent.com/98328584/150991795-9a4d406a-7f14-4143-bd98-4dbda34621f1.PNG)


# Created By
Dan Nylænder - Tellit Solutions - dan@tellitsolutions.no


# Concepts Covered
* Triggering a flow from PostMan using Webhook trigger
* Using Wanda Question action type to initiate dialogue with end user


# Actual usecase 

Tellit Solutions has developed an standard integration with ELMA (Peppol SMP) where we communicate with the end user through Wanda Questions if there is a need to update the customer register.
If the end user gives a positive response, we update the customer using the Customer REST API.


# Download Flows
The exported flow can be found in the following location, you will need both JSON files and these can be imported into your Extension Kit instance via the 'Import' button within the 'Flows' area.

[Flow Definitions](https://github.com/TellitSolutions/Tellit-Toolkit/tree/main/Extension%20Kit/Wanda%20Question/FlowDefinition)



