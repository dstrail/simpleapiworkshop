---
title: "Test your API"
chapter: false
weight: 80
---

To make sure that your API is working, you use [**curl**](https://curl.se/), a command line tool and library for transferring data with URLs.

## To get the URL to invoke your API:
1. Sign in to the API Gateway console at [https://console.aws.amazon.com/apigateway/](https://console.aws.amazon.com/apigateway)
2. Choose your API.
3. Note your API's invoke URL. It appears under Invoke URL on the Details page. 

![After you create your API, the console shows your API's invoke URL.](/images/ddb-invoke-url.png)
{{% notice note %}}
The full URL looks like this: https://**abcdef123**.execute-api.eu-west-1.amazonaws.com
{{% /notice %}}

4. **Copy your API's invoke URL.**

## To create or update an item:

1. Connect to Cloud9 by browsing to [https://console.aws.amazon.com/cloud9/](https://console.aws.amazon.com/cloud9/)
2. **Open the Cloud9 IDE** 
3. In the following command replace "https://**abcdef123**.execute-api.eu-west-1.amazonaws.com" with your Invoke URL from the previous step to set a variable with the **Invoke URL**

```bash
#DO NOT COPY THIS!!!
#Replace URL with the Invoke URL above
export INVOKE_URL="https://**abcdef123**.execute-api.eu-west-1.amazonaws.com"
```

4. Create or update an item. The command includes a request body with the item's ID, price, and name. 

```bash
curl -X "PUT" -H "Content-Type: application/json" -d "{
    \"id\": \"abcdef234\",
    \"price\": 12345,
    \"name\": \"myitem\"
}" $INVOKE_URL/items

```

{{%expand "**Challenge**: can you find the entry in DynamoDB?" %}}
1. Sign in to the DynamoDB console at [https://console.aws.amazon.com/DynamoDB/](https://console.aws.amazon.com/dynamodb)
2. Select Tables in the left pane
3. Select your table
4. Select Items tab
5. Confirm data from your PUT from previous step
{{% /expand%}}

## To get all items:

Use the following command to list all items.

```bash
curl -s $INVOKE_URL/items | js-beautify 
```

## To get an item:
Use the following command to get an item by its ID.

```bash
curl -s $INVOKE_URL/items/abcdef234 | js-beautify
```

## To delete an item:

Use the following command to delete an item.
```bash
curl -X "DELETE" $INVOKE_URL/items/abcdef234
```
Get all items to verify that the item was deleted.
```bash
curl -s $INVOKE_URL/items | js-beautify
```
