# Sila AuthToken Postman Collection

This Postman Collection is provided so that you can use and try out the [Sila Sandbox API](https://docs.silamoney.com/).

As a Sila customer, you must build your own application. **This Postman collection is only for testing purposes.**. We highly recommend that you review our documentation in the [Authentication Token Overview](https://docs.silamoney.com/docs/auth-token-overview) section before you begin testing in Postman.

## POSTMAN
This repository includes a Postman collection and a Postman environment. To use these, you will need to have the Postman desktop application installed: https://www.postman.com/downloads/. 

### Ensure your Postman installation is up to date
One known issue with importing this collection into older versions of Postman is that you may not have the `Authorization API` key option and will have to manually set the `Authorization` header on all requests (which is a pain, but you should still be able to use this collection).

### Import the collection and environment
To import the collection, there should be an Import button in the top left corner of the Postman application. Click this and browse to the `Sila_Sandbox.json` file in the postman folder of this repository.

To import the environment (which sets some defaults to make use of the collection easier), there should be a gear icon in the top right corner of the Postman application. When you click it, you should see an Import button. Click this and browse to the `Sila_Sandbox_Environment.json` file in the postman folder of this repository.

### Postman environment variables
Before you start making requests through Postman, you'll want to set some of these environment variables. You can set them by selecting the Postman environment you imported in the upper-right dropdown, hitting the eye icon, and hitting the Edit button. Here is an explanation of each variable - you can add your own and edit the collection locally as well.


| Variable Name                                                       | Default                       | Description                                      |
|---------------------------------------------------------------------|-------------------------------|--------------------------------------------------|
| backend_url                                                         | https://sandbox.silamoney.com | This is the url to which requests are forwarded. |
| app_name                                                            |                               | The name associated to your app.                 |
| app_handle                                                          |                               | This is the app handle you should have created in the Sila console. |
| app_client_id |                               | This is the Client ID associated to your app_handle |
| app_client_secret |                               | This is the Client Secret associated to your app_handle |
| user_handle |                               | This is a user handle which you can check for availability and register with a user's verification data. See our docs for more details. |
| team_id |                               | The ID associated to your team. |
| jwt_token |                               | The jwt_token can be obtained by called the Get Authentication Token endpoint in the Authentication Folder. |
| wallet_id |                               | The ID associated to an end user’s wallet. |
| business_handle | | A user handle that is registered as a business entity. |
| bank_account_name | | A bank account nickname associated to an end user’s linked bank account. |
| wallet_name | | The nickname associated to an end user’s wallet. |



## ENVIRONMENT SETUP
Begin with setting up your environment with the three variables listed below. You can retrieve your app_handle and app_client_id in the [Sila Console](https://console.silamoney.com/). The app_client_secret was provided when creating your app. For more details on how to access this information please visit our [Application Management](https://docs.silamoney.com/docs/console-application-management) documents.
* `app_handle`
* `app_client_id`
* `app_client_secret`

Afterwards, call the Get Authentication Token endpoint in the Authentication folder to receive the access token. Set the return token value to the `jwt_token` value in the environment. This will enable you to make successful requests for the other Sila Endpoints.
