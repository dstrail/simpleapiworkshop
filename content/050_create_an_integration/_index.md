---
title: "Create an integration"
chapter: false
weight: 50
---
![HTTP API gateway](/images/http-api-lambda.png)

You create an [**integration**](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-http.html) to connect a route to backend resources. At a later step you will attach these integrations to a route. For this example API, you create **one** Lambda integration that you use for all routes.

## Create an integration
1. Sign in to the API Gateway console at [https://console.aws.amazon.com/apigateway](https://console.aws.amazon.com/apigateway)
2. Choose your API (**http-crud-tutorial-api**)
3. Choose **Integrations**
4. Choose **Manage integrations** and then choose **Create**
![manage integration](/images/http-api-manage-integration.png)
5. Skip Attach this integration to a route. You complete that in a later step.
6. For Integration type, choose **Lambda function**
7. For Lambda function, enter `http-crud-tutorial-function`
![integration target](/images/http-api-integration-target.png)

8. Choose **Create**
