---
title: "Create an integration"
chapter: false
weight: 60
---

You create an integration to connect a route to backend resources. For this example API, you create one Lambda integration that you use for all routes.

##### To create an integration
1. Sign in to the API Gateway console at https://console.aws.amazon.com/apigateway
2. Choose your API.
3. Choose Integrations.
4. Choose Manage integrations and then choose Create.
5. Skip Attach this integration to a route. You complete that in a later step.
6. For Integration type, choose Lambda function.
7. For Lambda function, enter 
```bash
     http-crud-tutorial-function
```
8. Choose Create.
