---
title: "Test your API"
chapter: false
weight: 80
---

To make sure that your API is working, you use [**curl**](https://curl.se/)

##### To get the URL to invoke your API:
1. Sign in to the API Gateway console at https://console.aws.amazon.com/apigateway
2. Choose your API.
3. Note your API's invoke URL. It appears under Invoke URL on the Details page. 

![After you create your API, the console shows your API's invoke URL.](/images/ddb-invoke-url.png)

4. Copy your API's invoke URL.

The full URL looks like https://**abcdef123**.execute-api.eu-west-1.amazonaws.com.

##### To create or update an item:

Use the following command to create or update an item. The command includes a request body with the item's ID, price, and name. 

```bash
    curl -v -X "PUT" -H "Content-Type: application/json" -d "{\"id\": \"abcdef234\", \"price\": 12345, \"name\": \"myitem\"}" https://abcdef123.execute-api.us-west-2.amazonaws.com/items
```

##### To get all items:

Use the following command to list all items.

```bash
    curl -v https://abcdef123.execute-api.us-west-2.amazonaws.com/items
```

##### To get an item:
Use the following command to get an item by its ID.

```bash
    curl -v https://abcdef123.execute-api.us-west-2.amazonaws.com/items/abcdef234
```

##### To delete an item:

1. Use the following command to delete an item.
```bash
    curl -v -X "DELETE" https://abcdef123.execute-api.us-west-2.amazonaws.com/items/abcdef234
```
2. Get all items to verify that the item was deleted.
```bash
    curl -v https://abcdef123.execute-api.us-west-2.amazonaws.com/items
```
