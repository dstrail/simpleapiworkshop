---
title: "Attach your integration to routes"
chapter: false
weight: 60
pre: "<b>6. </b>"
---

![HTTP API to DDB](/images/ddb-crud.png)

For this example API, you use the same [**AWS Lambda integration**](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-lambda.html) for all routes. After you attach the integration to all of the API's routes, your Lambda function is invoked when a client calls any of your routes.

## To attach integrations to routes

1. Sign in to the API Gateway console at [https://console.aws.amazon.com/apigateway](https://console.aws.amazon.com/apigateway)
2. Choose your API (**http-crud-tutorial-api**)
3. Choose **Integrations**
4. Choose a route
5. Under Choose an existing integration, choose `http-crud-tutorial-function`
![choose integration](/images/http-api-choose-integration.png)
6. Choose **Attach integration**
7. **Repeat** steps 4-6 for all routes. All routes show that an AWS Lambda integration is attached.

![The console shows AWS Lambda on all routes to indicate that your integration is attached.](/images/http-api-all-integration.png)

Now that you have an HTTP API with routes and integrations, you can **test your API**.