---
title: "Welcome"
chapter: true
weight: 1
---

In the next few pages we will get started on creating your API. The steps include: 

- Creating a DynamoDB table using the DynamoDB console
- Creating a Lambda function in the AWS Lambda console
- Creating an HTTP API using the API Gateway console 
- Testing your API!

When you invoke your HTTP API, API Gateway routes the request to your Lambda function. The Lambda function interacts with DynamoDB, and returns a response to the API Gateway. The API Gateway then returns a response to you. 

![Architectural overview of the API that you create in this tutorial. Clients use an API Gateway HTTP API to invoke a Lambda function. The Lambda function interacts with DynamoDB and then returns a response to clients. ](/images/ddb-crud.png)

If you are at an AWS hosted event (such as re:Invent, ServerlessDays, an Immersion Day, or any other event hosted by an AWS employee) you can follow the instructions on: 

[Use the AWS workshop portal](./aws_event/). 

If you are running this event on your own then go to:

[Start the workshop on your own](./self_hosted/).


