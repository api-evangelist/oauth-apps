# Saleforce OAuth
This is a walk through of setting up a Salesforce OAuth application so you can use in a Postman collection for making requests to the Salesforce REST API. There are several ways you can authenticate with Salesforce and this way walks you through the OAuth 2.0 approach to authorization with the Salesforce REST API with a full connected application setup.

You can manage your connected applications within your Salesforce account under Platform Tools > Apps > App Manager. You can manage your existing application using the listing or you can create a new one using the New Connected App button in the top right corner of the screen.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-collections/salesforce/1-salesforce-app-manager.png "Salesforce App Manager")

When adding your application you will not need to fill out every single field, but there are handful that are required before you can actually hit add. You must give it an app and API name, as well as provide your contact email. After that, make sure you also click on "Enable OAuth Settings", otherwise you will not get what you need to authenticate using Postman.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-collections/salesforce/2-salesforce-app-manager-setup-1.png "Salesforce App Manager Setup")

After entering this basic information scroll down a bit, and you will need add the callback URL for your app, which in this case is Postman, so just add https://app.getpostman.com/oauth2/callback. Next you will have choose your OAuth scopes--if unsure select Full Access, which will give you access to everything you need.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-collections/salesforce/3-salesforce-app-manager-setup-.png "Salesforce App Manager Setup")

Go ahead and save your application, and then you will be dropped on the screen with the details of your new Salesforce OAuth Connected API. This page contains all the settings you will need to enable Postman, and setup the proper authorization to begin working with your Salesforce installation via the Salesforce REST API.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-collections/salesforce/4-salesforce-app-manager-settings.png "Salesforce App Manager Settings")

Next, head to your Postman application, and either navigate to the Salesforce collection you are working with, or create a new collection. Once you have your collection in the Postman navigation pane, click on the arrow to edit the collection settings, so that we can enter our authorization settings.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-collections/salesforce/5-salesforce-postman-edit.png "Postman")

Once the settings window for your collection is open you will need to navigate to the authorization tab, which will have the settings we need to add from the Salesforce OAuth Connected App we just setup using our Salesforce account.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-collections/salesforce/6-salesforce-postman-authorization.png "Postman Authorization")

Once we are on the Postman authorization tab for our collection we are are going to need to enter all of the settings we generated as part of our Salesforce oAuth Connected Application, entering token a name, a grant type of authorization code, the callback URL, auth URL, access token URL, client id, and client secret.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-collections/salesforce/7-salesforce-authorization-settings.png "Postman Authorization Settings")

Go ahead and request a token which will take you to login to Salesforce and do the oAuth dance that will ultimately generate the token we will need to make our request. Salesforce tokens are not very long lived, so this is a process that we will have to repeat each time we use our collection, but it is a simple regeneration process, not the entire application setup.
