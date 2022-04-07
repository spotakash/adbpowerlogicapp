# Building Native OAuth2.0 based Flow Integration with Azure Databricks

In this small repo, we are trying to show how easy and out-of-box to set up OAuth2.0 based Microsoft Flow integration with Azure Databricks.

    # Note: Same approach (almost 99.9%) can be repeated if you are using Azure Logic App for building any Businss Integration Solution

Scenario: 

- *End User to System:* There is front end portalm which can be accessed by authorized user. This portal has one interface which is nothing just some function <code/ or javascript/ let's take example>. User can interract can trigger this function by feeding information or it can be static function without input (use case be anything). 

- *Portal to Flow:* Once function trigger, it basically trigger Microsoft Flow behind the scene (Logic App equivalent in Azure, based upon http request). 

- *
