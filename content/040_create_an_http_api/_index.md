---
title: "Create an http API"
chapter: false
weight: 40
---

The HTTP API provides an HTTP endpoint for your Lambda function. In this step, you create an empty API. In the following steps, you configure routes and integrations to connect your API and your Lambda function. 

##### To create an HTTP API:
1. Sign in to the API Gateway console at [https://console.aws.amazon.com/apigateway](https://console.aws.amazon.com/apigateway)
2. Choose Create API
![Create API](/images/create-API.png) 
3. For HTTP API choose Build 
![HTTP API](/images/http-api.png)
4. For API name, enter http-crud-tutorial-api.
![api name](/images/api-name.png)
5. Choose Next.
6. For **Configure routes**, choose Next to skip route creation. You create routes later.
7. Review the stage that API Gateway creates for you ($default), and then choose Next.
8. Choose Create.

![successfully created an API gateway](/images/successfully-created-apigw.png)

