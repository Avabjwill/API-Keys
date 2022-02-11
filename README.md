# How to Use API Keys
This document describes API Keys with OpenWeather API by using Server-side calls. This document does not describe the use of Client Side API.

# Server Side API 
*Server-side APIs* allow developers to access data made available by third-party companies and organizations. The reason the APIs are called server-side APIs is because the code executes on the server before being is sent to the browser.

To use the data, developers can create applications that:
- Make requests to URLs, or endpoints

APIs provide access to data within the given extent they have, but they're added to the HTTP request in different places.

There are two types of credentials you can use to access API end-point data:

- API keys are long-lasting credentials that can be revoked by users
- JWT tokens are short-lived, expiring credentials

In time, you'll learn how to create these requests on the  server-side of your application. 


## TABLE OF CONTENTS

- [SERVER SIDE API](#server-side-api)
- [REQUEST AN API KEY](#request-an-api-key)
- [CREATE VARIABLES FOR API KEY](#create-variables-for-api-key)
- [CONSTRUCT A QUERY TO MAKE THE API CALL](#construct-a-query-to-make-the-api-call)
- [PASSING PARAMETERS](#passing-parameters)
- [MAKE AN API CALL](#make-an-api-call)

# Request an API Key
You can generate an API Key with the OpenWeather API. (To request an API Key you will need an [OpenWeather Account](https://openweathermap.org/api)

You can give your API key a name that's unique to be generated. Copy the new API Key that you've created, and save the API Key in the JavaScript file where you'll be making API calls.

# Create a Variable to Store the API Key
Now that you can store the API Key in a variable so that the API Key can be reused in your code.

The variable will resemble the following code snippet:

```sh
var APIKey = "12341234123412341234123412341234";
```

**Note**: The variables name is APIKey

# Create Variables for the API Call
Depending on the API call you will need to include different *query* parameters.

In the API call reference below using the Current Weather Data portion of the OpenWeather API, you can search by city name.

You will collect user input for the city name and store in a variable, as shown in the following:

```sh
var city;
```

# Construct a Query URL to Make the API Call
You can construct a query URL, which will be used to make the API call.

To use other data points from the API, you'll need to use the URL listed in [OpenWeather Current Weather Data documentation](https://openweathermap.org/current#name)

Make an API call using the city name.

Sample Response:

```sh
api.openweathermap.org/data/2.5/weather?q={city name}&appid={API key}
```

Replace the relevant placeholders in the URL with your variables.

# Passing Parameters

Parameters are the variable terms that you can add to an API call to specify the data you want to request.

##  **q**: The **query** parameter, where you'll add the city variable.

##  **appid**: The **application idor** where you'll add the API key variable.

In the API reference below create a new variable queryURL.

```sh
var queryURL = "http://api.openweathermap.org/data/2.5/weather?q=" + city + "&appid=" + APIKey;
```

To call your API you can construct a variable to hold your query URL.
