---
title: REST API - Postman
nav_text: Postman
heading: REST API - Postman
description: REST API - Postman
variables:
  ItemKey: features/rest_api/test_environment_postman.htm
---


REST APIs are available as a Postman collection. To start working with REST APIs, import the collection into Postman and complete a simple setup procedure.

## Before You Begin

Download the Postman application from the $[Postman](https://www.getpostman.com/) website, and install it on a computer that can communicate with the Global Server computer.

## Procedure

1. Import the REST API collection into your Postman application:

    - To open the collection directly in the Postman application, open $[Rest API \- Public](https://api.example.com/) in your browser, and then click the **Run in Postman** button \(in the upper\-right of the page\).

    - To download the collection and manually import it into the Postman application, choose one of the following:

        - File hosted on GitHub: $[Rest\-API\-Postman\-Collection](https://github.com/ExampleRepo/Rest-API-Postman-Collection)

        - If you are not connected to the internet, download the local file: $[Host\_Rest\_API\_V1\_Public\_postman\_collection.json](file:features/rest_api/JSON/Host_Rest_API_V1_Public_postman_collection.json)

    To view documentation for the Postman collection, see $[Host Rest API \- Public](https://api.example.com/).

2. In the Postman application, create an environment.

    For information on creating an environment, go to the $[Postman](https://www.getpostman.com/docs/postman/environments_and_globals/manage_environments) website, *Manage environments*.

3. In the REST API collection, open the **0 \- Setup** folder and click the **Environment Setup** API.

4. On the **Pre\-request Script** tab, update the predefined variables with your user name, your Base64 encoded password, and your Web Service URL.

    For information on the Web Service URL, see $[Available Web Services for REST API](https://documentation.example.com/essential/45592.htm).

5. To run the API, click **Send**.

    The **Environment Setup** API returns an authentication token. The token, your user name, your Base64 encoded password, and your Web Service URL are saved as environment variables.
