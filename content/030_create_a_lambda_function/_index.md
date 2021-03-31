---
title: "Create a lambda function"
chapter: false
weight: 30
---

[**AWS Lambda**](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)  is a compute service that lets you run code without provisioning or managing servers. Lambda runs your code only when needed and scales automatically, from a few requests per day to thousands per second.

You create a Lambda function for the backend of your API. This Lambda function **c**reates, **r**eads, **u**pdates, and **d**eletes (**CRUD**) items from DynamoDB. The function uses [**events from API Gateway**](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-lambda.html#http-api-develop-integrations-lambda.proxy-format) to determine how to interact with DynamoDB. For simplicity this tutorial uses a single Lambda function. As a best practice, you should create separate functions for each route. 



##### To create a Lambda function:
1. Sign in to the Lambda console at [https://console.aws.amazon.com/lambda](https://console.aws.amazon.com/lambda)
2. Choose Create function.
3. For Function name, enter `http-crud-tutorial-function`
4. Under Permissions choose Change default execution role
5. Select Create a new role from AWS policy templates
6. For Role name, enter `http-crud-tutorial-role`
7. For Policy templates, choose Simple microservice permissions. This policy grants the Lambda function permission to interact with DynamoDB. 


{{% notice warning %}}

This workshop uses a managed policy for simplicity. As a best practice, you should create your own IAM policy to grant the minimum permissions required. 

{{% /notice %}}


8. Choose Create function
9. Open index.js in the console's code editor, and replace its contents with the following code. Choose Deploy to update your function. 

```bash
const AWS = require("aws-sdk");

const dynamo = new AWS.DynamoDB.DocumentClient();

exports.handler = async (event, context) => {
  let body;
  let statusCode = 200;
  const headers = {
    "Content-Type": "application/json"
  };

  try {
    switch (event.routeKey) {
      case "DELETE /items/{id}":
        await dynamo
          .delete({
            TableName: "http-crud-tutorial-items",
            Key: {
              id: event.pathParameters.id
            }
          })
          .promise();
        body = `Deleted item ${event.pathParameters.id}`;
        break;
      case "GET /items/{id}":
        body = await dynamo
          .get({
            TableName: "http-crud-tutorial-items",
            Key: {
              id: event.pathParameters.id
            }
          })
          .promise();
        break;
      case "GET /items":
        body = await dynamo.scan({ TableName: "http-crud-tutorial-items" }).promise();
        break;
      case "PUT /items":
        let requestJSON = JSON.parse(event.body);
        await dynamo
          .put({
            TableName: "http-crud-tutorial-items",
            Item: {
              id: requestJSON.id,
              price: requestJSON.price,
              name: requestJSON.name
            }
          })
          .promise();
        body = `Put item ${requestJSON.id}`;
        break;
      default:
        throw new Error(`Unsupported route: "${event.routeKey}"`);
    }
  } catch (err) {
    statusCode = 400;
    body = err.message;
  } finally {
    body = JSON.stringify(body);
  }

  return {
    statusCode,
    body,
    headers
  };
};

```
