# Web development

## Part 1

Write a web server app with a single endpoint `/hello` that returns HTTP 200 and text `Hello`

## Part 2

Change the endpoint to accept an optional `name` param, and use that in the response when available.

`/hello?name=Bruce`

```
HTTP 200

Hello Bruce
```

## Part 3

Introduce a path variable for language, to respond hello in any supported languages.

`/en-US/hello?name=Akash` -> `Hello Akash`

`/fr-FR/hello?name=Akash` -> `Bonjour Akash`

`/en-AU/hello?name=Akash` -> `G'day Akash`

`/it-IT/hello?name=Akash` -> `Salve Akash`

`/en-GB/hello?name=Akash` -> `Alright, Akash?`

## Part 4

Create a new endpoint `/echo_headers` which returns a list of all request headers as the response text

Send some custom headers using curl, Postman or other HTTP/API client app.

Example response:

```
Accept: text/html
Accept-Encoding: gzip
Connection: keep-alive
Accept-Language: en-GB
...
...
```

## Part 5

Change the endpoint `/hello?name=Bruce` (without language path variable) to read the `Accept-Language` header and respond in the appropriate languages. Only support the previously listed languages.

## Part 6

If not done already, write fast, isolated tests for the above functionality.

## Part 7

Write a HTTP client for the server implemented above.

The client should be a class, with a method for each of the above functionalities.

e.g. (pseudocode)

```
val client = MyHttpClient(baseUrl="http://localhost")

client.hello(name="Bruce", language="en-US") // should return "Hello Bruce"
```