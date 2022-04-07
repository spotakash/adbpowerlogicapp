# Building Native OAuth2.0 based Flow Integration with Azure Databricks

In this small repo, we are trying to show how easy and out-of-box to set up Azure Active Directory (AAD) OAuth2.0 based Power Apps Flow integration with Azure Databricks.

    # Note: Same approach (almost 99.9%) can be repeated if you are using Azure Logic App for building any Businss Integration Solution

## Scenario:

- *End User to System:* There is front end portal which can be accessed by authenticated/authorized user from Azure AD (AAD). This portal has one interface which is nothing but some function or code button <behind the scene code/ or javascript/ let's assume>. User can interract can trigger this function by feeding information or it can be static function without input (use case be anything). 

- *Portal to Power Apps Flow:* Once function trigger, it basically trigger Microsoft Flow behind the scene (Logic App equivalent in Azure, based upon http request). Gone are those days, where we need to club everything together. Using Flow/Logic App, application process can be easily de-coupled. 

- *Power Apps Flow to Azure Databricks (ADB):* Now comes the interesting part, ADB can be non-interactively consumed from using various ways. In this repo, we shall how Natively Flow can talk to ADB and seamless OAuth token exchange happen and query execution happen.


## High Level Design

Using combination of various component. We can achieve seamless secure natively authenticatd request flow to ADB. 

![](Architecture/ADBPowerApp.jpg)

### Components in Play
- Power Apps Customer Connector
- Power Apps Flow
- Azure Databricks 
- Azure Active Directory Application
- Azure Active Directory Application API Permission

> Assumption: You have Power Apps Portal already set up. We shall only show how to set up integration Flow to ADB

### Steps

> Assumption: You have AAD Application Created for ADB which will be consumed by Power App Flows Conenctor and have noted down Application ID and Associated Secret. 

1. Build Custom Connector

    1.1. Add Custom Connect
    
    1.2. Add Securtiy Details

    1.3 Update AAD Application Return URL

    1.4 Add AAD Application API Permission for ADB

    1.5 Add Definition

    1.6 Test Connector

2. Create Connection

3. Create Flow and Test Connection




