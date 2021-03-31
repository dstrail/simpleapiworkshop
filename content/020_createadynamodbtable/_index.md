---
title: "Create a DynamoDB table"
chapter: false
weight: 20
---

You use an [**Amazon DynamoDB**](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html) table to store data for your API. 
Each item has a unique ID, which we use as the [**partition key**](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html#HowItWorks.CoreComponents.PrimaryKey) for the table. 


**To create a DynamoDB table:** 
1. Open the DynamoDB console at https://console.aws.amazon.com/dynamodb/ 
2. Choose Create table.
3. For Table name, enter http-crud-tutorial-items.
4. For Primary key, enter id.
5. Choose Create.

  