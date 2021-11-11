# ExternalIdentitiesGovernance

Repository for Azure AD Identity Governance and External Identities Self Service.

## Contents

This repository contains demo instructions and resources from where I have presented this solution to the community, either reference by a session in a conference or in any blog posts.

This repo contains:

* Logic App code for reference for a custom extension for an Access Package in Identity Governance.
* An adaptive card I used in the Logic App for sending a card to a Teams channel as a bot.
* Overview over demo instructions.
### Demo Script

The following step by step is an overview over a demo set up, the details can be left for you to decide.

1. In Entitlement Management, use or create a Catalog enabled for external users.
1. Set up or configure a Connected Organization for a partner/demo tenant where you want external identities to sign up from. Configure any internal or external sponsors.
1. Add any Resources (Teams, Apps, Sites) to this Catalog that you want to create Access Packages for.
1. Create an Access Package for your Demo scenario, containing the Resources you want and with customizations for questions and lifecycle/approval settings.
1. Make sure the Access Package is enabled for requests, and then test a request from your connected organization. 
1. Approve the request, and verify that the external user is added to your Azure AD as a Guest user, and added to the selected Resources in the Access Package.

**Demo part 2:**

1. In Entitlement Management, open the Catalog, and a a Custom Extension.
1. Enter a Name and Description, and under Details create a new Logic App, a new Azure AD Application, and specify the Azure Subscription, Resource Group and Logic App name.
1. Create the Logic App and validate to create the Custom Extension workflow.
1. This Logic App can now be extended to your needs, for example send a message to a Team or other integrations you want. A Logic App sample is included in this repo.
1. For the Access Package you , edit the policy (Initial Policy or any other custom policies you need), and under Rules, add the Stages you want and link the Custom Extension to trigger the Logic App.
1. You can now test another external request and check that the Logic App is triggered.
