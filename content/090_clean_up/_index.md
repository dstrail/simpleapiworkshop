---
title: "Clean UP!"
chapter: false
weight: 90
---

To prevent unnecessary costs, delete the resources that you created as part of this getting started exercise. The following steps delete your HTTP API, your Lambda function, and associated resources.

{{% notice info %}}

If this is an event organized by AWS, you don't need to follow the steps below. The environment will be terminated after the event has concluded.

{{% /notice %}}

## To delete an DynamoDB table:

1. Open the DynamoDB console at https://console.aws.amazon.com/dynamodb/
2. Select your table.
3. Choose Delete table.
4. Confirm your choice, and choose Delete.

## To delete an HTTP API:

1. Sign in to the API Gateway console at https://console.aws.amazon.com/apigateway
2. On the APIs page, select an API. Choose Actions, and then choose Delete.
3. Choose Delete.


## To delete a Lambda function:

1. Sign in to the Lambda console at https://console.aws.amazon.com/lambda
2. On the Functions page, select a function. Choose Actions, and then choose Delete.
3. Choose Delete.

## To delete a Lambda function's log group:

1. In the Amazon CloudWatch console, open the [**Log groups page**](https://console.aws.amazon.com/cloudwatch/home#logs:)
2. On the Log groups page, select the function's log group (/aws/lambda/http-crud-tutorial-function). Choose Actions, and then choose Delete log group.
3. Choose Delete.

## To delete a Lambda function's execution role:

1. In the AWS Identity and Access Management console, open the [**Roles page**](https://console.aws.amazon.com/iam/home?#/roles)
2. Select the function's role, for example, http-crud-tutorial-role.
3. Choose Delete role.
4. Choose Yes, delete.

