# Twitter OAuth
This is a walk through for setting up a Twitter application so that you can authorize using Postman. Before you can use any Postman Twitter API collection you will have to download the Postman applications, then setup your own Twitter application at: https://developer.twitter.com/en/apps so you can make calls to the Twitter API--do not worry, it is painless, and something even a non-developer can do.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-tutorials/twitter-status-lookup/twitter-application.png "New Application")

When filling out the form, all you need is to give your app a name, description, website URL, and tell them how it will be used. You can ignore the rest of the fields. Once the application is added you can obtain your access tokens by clicking on the keys and tokens tab.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-tutorials/twitter-status-lookup/twitter-keys-and-tokens.jpg "Keys and Tokens")

The first time you create your application you will have regenerate your access token and access token secret, and then you will need all four tokens to authenticate (Don't worry those aren't my real tokens). Once you have your own tokens, go back to your Postman application and click on the Twitter Lookup Postman collection, and edit its details.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-tutorials/twitter-favorites/twitter-favorites-edit.png "Edit Collection")

Once the edit window pops up select the Authorization tab, then select to use OAuth 1.0 and add your auth data to request headers from the dropdown boxes, then add your own {{consumer_key}}, {{consumer_secret}}, {{access_token}}, and {{token_secret}} from the application you setup.

![alt text](https://kinlane-productions.s3.amazonaws.com/postman-tutorials/twitter-favorites/twitter-favorites-auth.png "Edit Collection Authorization")

Once you have entered all your tokens you should be able to make a Twitter API request using any endpoint added to a Postman collection. While this OAuth setup was meant for Postman, the same steps can be used in any application or custom code as well, as the process is meant to be standardized for any integration. In this case, Postman is the application.
