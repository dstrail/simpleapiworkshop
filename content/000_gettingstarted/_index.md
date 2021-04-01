---
title: "Welcome"
chapter: true
weight: 1
---

Your goal in this workshop is to build a very simple CRUD API (your first API?). To accomplish this you will be guided through a few steps. Starting with creating a DynamoDB table using the DynamoDB console, to creating a Lambda function in the AWS Lambda console. Next you will configure an HTTP API using the API Gateway console and last, after launching an AWS Cloud9 IDE you will use it to test your API!

If you have little experience with AWS but know your way around at typing commands in a terminal, this workshop is for you! (Copy/Paste allowed!) 

![Architectural overview of the API that you create in this tutorial. Clients use an API Gateway HTTP API to invoke a Lambda function. The Lambda function interacts with DynamoDB and then returns a response to clients. ](/images/ddb-crud.png)
When you invoke your HTTP API, API Gateway routes the request to your Lambda function. The Lambda function interacts with DynamoDB, and returns a response to the API Gateway. The API Gateway then returns a response to you. 

### Next: 
If you are at an AWS hosted event (such as re:Invent, ServerlessDays, an Immersion Day, or any other event hosted by an AWS employee) you can follow the instructions on: 

[Use the AWS workshop portal](./aws_event/). 

If you are running this event on your own then go to:

[Start the workshop on your own](./self_hosted/).


