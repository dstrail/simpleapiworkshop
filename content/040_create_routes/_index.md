---
title: "Create routes"
chapter: false
weight: 50
---
![HTTP API gateway](/images/http-api-lambda.png)

[**Routes**](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-routes.html) are a way to send incoming API requests to backend resources. Routes consist of two parts: an HTTP method and a resource path, for example, GET /items. For this example API, we create four routes:

**GET** `/items/{id}`

**GET** `/items`

**PUT** `/items`

**DELETE** `/items/{id}`

## Create routes:
1. Sign in to the API Gateway console at [https://console.aws.amazon.com/apigateway](https://console.aws.amazon.com/apigateway)
2. Choose your API (http-crud-tutorial-api)
3. On the left panel choose Routes 
4. Choose Create.
![Create routes](/images/http-api-create-route.png)

5. For **Method**, choose **GET**
![get route](/images/http-api-get-route.png)
6. For the **path**, enter `/items/{id}`. The {id} at the end of the path is a path parameter that API Gateway retrieves from the request path when a client makes a request.
7. Choose **Create**
8. **Repeat** steps 4-7 for **GET** `/items`, **DELETE** `/items/{id}`, and **PUT** `/items`.
![delete route](/images/http-api-delete-route.png)
9. Confirm all routes are created

![Your API has routes for GET /items, GET /items/{id},DELETE /items/{id}, and PUT /items.](/images/http-api-routes.png)