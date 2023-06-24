# Login2Xplore


# Student Enrollment Form

It is a student registration form that saves the user's information in JSONPowerDB. Both serverless technology and REST APIs are supported. A student's roll number can be used to add or update them. The roll number is automatically verified on this form, and with the use of an API, the data submitted into other input fields is also verified so that the user can change as necessary. AJAX requests are used by the programme to enable quick and seamless interaction. Data of every kind, including numbers, strings, dates, and more, can be saved.

## Benefits of using JsonPowerDB
- Simplest way to retrieve data in a JSON format.
- Schema-free, Simple to use, Nimble and In-Memory database.
- It is built on top of one of the fastest and real-time data indexing engine - PowerIndeX.
- It is low level (raw) form of data and is also human readable.
- uses a variety of tools and strategies to assist developers in maintaining their databases.



# Release History

## JsonPowerDB

### Version: 1.0

#### Execute API

```javascript
var baseUrl = "http://api.login2explore.com:5577";
function executeCommand(reqString, apiEndPointUrl) {
    var url = baseUrl + apiEndPointUrl;
    var jsonObj;
    $.post(url, reqString, function (result) {
        jsonObj = JSON.parse(result);
    }).fail(function (result) {
        var dataJsonObj = result.responseText;
        jsonObj = JSON.parse(dataJsonObj);
    });
    return jsonObj;
}
```
## Create a PUT Request String

```javascript
function createPUTRequest(connToken, jsonObj, dbName, relName) {
    var putRequest = "{\n"
            + "\"token\" : \""
            + connToken
            + "\","
            + "\"dbName\": \""
            + dbName
            + "\",\n" + "\"cmd\" : \"PUT\",\n"
            + "\"rel\" : \""
            + relName + "\","
            + "\"jsonStr\": \n"
            + jsonObj
            + "\n"
            + "}";
    return putRequest;
}

```
## Features

- Simple to Use
- Fast Response
- Detailed User Interface


## Tech Stack

**Client:** 
>HTML
>CSS
>Javascript

**Server:** 
>JsonPowerDB
