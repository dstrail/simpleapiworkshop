---
title: "Attach your integration to routes"
chapter: false
weight: 70
---



For this example API, you use the same Lambda integration for all routes. After you attach the integration to all of the API's routes, your Lambda function is invoked when a client calls any of your routes.

##### To attach integrations to routes

1. Sign in to the API Gateway console at https://console.aws.amazon.com/apigateway
2. Choose your API.
3. Choose Integrations.
4. Choose a route.
5. Under Choose an existing integration, choose http-crud-tutorial-function.
6. Choose Attach integration.
7. Repeat steps 4-6 for all routes.

All routes show that an AWS Lambda integration is attached.

![The console shows AWS Lambda on all routes to indicate that your integration is attached.](/images/ddb-attach-integrations.png)

Now that you have an HTTP API with routes and integrations, you can test your API.