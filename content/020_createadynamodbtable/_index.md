---
title: "Create a DynamoDB table"
chapter: false
weight: 20
---


![dyanmodb](/images/ddb.png)

[**Amazon DynamoDB**](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html) is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. DynamoDB lets you offload the administrative burdens of operating and scaling a distributed database so that you don't have to worry about hardware provisioning, setup and configuration, replication, software patching, or cluster scaling. 

With Amazon DynamoDB, you can create database [**tables**](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithTables.Basics.html) that can store and retrieve any amount of data and serve any level of request traffic.

You use an Amazon DynamoDB table to store data for your API. 
Each item has a unique ID, which we use as the [**partition key**](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html#HowItWorks.CoreComponents.PrimaryKey) for the table. 


To **create a DynamoDB table**:
1. Open the DynamoDB console at [https://console.aws.amazon.com/dynamodb/](https://console.aws.amazon.com/dynamodb/)
2. Choose Create table
![dyanmodb create](/images/dynamodb-create.png)
3. For Table name, enter `http-crud-tutorial-items`
4. For Primary key, enter `id` 
5. Choose Create (see below: 1,2,3)
![dyanmodb create table](/images/dynamodb-create-table.png)


  After a few seconds your DynamoDB table becomes available. 