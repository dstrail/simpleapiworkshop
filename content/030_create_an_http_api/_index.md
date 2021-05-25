---
title: "Create an http API"
chapter: false
weight: 30
pre: "<b>3. </b>"
---
![HTTP API gateway](/images/http-api-client.png)
[**Amazon API Gateway**](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html) is a fully managed service that makes it easy for developers to publish, maintain, monitor, secure, and operate APIs at any scale. 

With API Gateway, you can create RESTful APIs using either HTTP APIs or REST APIs. Together with AWS Lambda, API Gateway forms the app-facing part of the [**AWS serverless**](https://aws.amazon.com/serverless/) infrastructure.

HTTP APIs enable you to create RESTful APIs with lower latency and lower cost than REST APIs.
You can use HTTP APIs to send requests to AWS Lambda functions or to any publicly routable HTTP endpoint. 

The HTTP API provides an HTTP endpoint for your Lambda function. In this step, you create an empty API. In the following steps, you configure routes and integrations to connect your API and your Lambda function. 

## Create an HTTP API:
1. Sign in to the API Gateway console at [https://console.aws.amazon.com/apigateway](https://console.aws.amazon.com/apigateway)
2. Choose Create API (If you see a welcome screen skip this step and go to step 3)
![Create API](/images/create-API.png) 
3. For HTTP API choose Build 
![HTTP API](/images/http-api.png)
4. For API name, enter `http-crud-tutorial-api`
![api name](/images/api-name.png)
5. Choose Next.
6. For **Configure routes**, choose Next to skip route creation. You create routes later.
7. Review the stage that API Gateway creates for you ($default), and then choose Next.
8. Choose Create.

![successfully created an API gateway](/images/successfully-created-apigw.png)

