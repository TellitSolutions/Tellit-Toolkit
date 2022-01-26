# Two step authentication

Many external APIs requires that you authenticate using a "two-step authentication" method.
This examples shows how this can be implemented in Extension Kit.

This example uses the Creditsafe APIs, and you would need a test account with Creditsafe to run this example.
However, the process would be very similar for any 3rd party API requiring this method of authentication.

The "Two-step authentication" process works in the following way:

Step 1: Get the authentication token based on provided username and password:
![Retrieving Auth Token](https://user-images.githubusercontent.com/98328584/151136925-a83b7abe-7120-4290-b556-875d424a00a4.PNG)


Step 2: Assign the given authentication token in the header-section when doing subsequent API-calls to the 3rd party vendor:
![Sending auth token in header](https://user-images.githubusercontent.com/98328584/151137073-32eba976-80e3-4351-84a7-907d90581227.PNG)



# Created By
Dan Nylænder - Tellit Solutions - dan@tellitsolutions.no



# Concepts Covered
* Triggering a flow from a Message Hub Event in ERPx
* Two step authentication against an external API



# Actual usecase 

Tellit Solutions has developed a global solution in Extension Kit to do credit checks on both customers and suppliers in Unit4 ERP. 
These solutions are compliant with both ERP7 and ERPx and are developed using Creditsafe APIs, which allows us to do credit checks on almost 400 million companies in over 160 countries.



# Download Flows
The exported flow can be found in the following location, you will need both JSON files and these can be imported into your Extension Kit instance via the 'Import' button within the 'Flows' area.

[Flow Definitions](https://github.com/TellitSolutions/Tellit-Toolkit/tree/main/Extension%20Kit/Two%20Step%20Authentication/FlowDefinition)



