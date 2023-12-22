# Web development

For each part, you can test the server manually by running the app, and using a browser or HTTP/API client like curl or Postman.

You should also write automated tests for each part. In some technologies (such as http4k), you can test the server in memory without explicitly starting it.

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

Change the endpoint to introduce a path variable for language, to respond hello in any supported languages.

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

Change the `echo_headers` endpoint so that if the client supports JSON responses, respond with a JSON response body with the headers as key-value pairs.

Research how an HTTP client indicates what response types it supports.

## Part 6

For the `echo_headers` endpoint, accept a query param `?as_response_headers_with_prefix=X-Echo-`

When this query param is present, there is no response text. Instead, the request headers are echoed back as response headers, but with the given prefix attached to the header name.

e.g. for `?as_response_headers_with_prefix=X-Echo-`, if a header `X-My-Custom-Header: some value` was present in the request, then there should be a header `X-Echo-X-My-Custom-Header: some value` present in the response.

## Part 7

Change the hello endpoint to remove the path variable and instead read the `Accept-Language` header and respond in the appropriate languages.

## Part 8

Write a HTTP client for the server implemented above.

The client should be a class, with a method for each of the above functionalities.

e.g. (pseudocode)

```
val client = MyHttpClient(baseUrl="http://localhost")

client.hello(name="Bruce", language="en-US") // should return "Hello Bruce"
```
