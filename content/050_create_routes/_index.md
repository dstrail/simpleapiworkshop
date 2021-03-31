---
title: "Create routes"
chapter: false
weight: 50
---


Routes are a way to send incoming API requests to backend resources. Routes consist of two parts: an HTTP method and a resource path, for example, GET /items. For this example API, we create four routes:

    GET /items/{id}

    GET /items

    PUT /items

    DELETE /items/{id}

##### To create routes:
1. Sign in to the API Gateway console at https://console.aws.amazon.com/apigateway
2. Choose your API.
3. Choose Routes.
4. Choose Create.
5. For Method, choose GET.
6. For the path, enter /items/{id}. The {id} at the end of the path is a path parameter that API Gateway retrieves from the request path when a client makes a request.
7. Choose Create.
8. Repeat steps 4-7 for GET /items, DELETE /items/{id}, and PUT /items.

![Your API has routes for GET /items, GET /items/{id},DELETE /items/{id}, and PUT /items.](/images/ddb-create-routes.png)
