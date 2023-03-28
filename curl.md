# Curl Basics

## Basic Syntax
The basic syntax of curl is:


```console
foo@bar:~$ curl [options] [URL]
foo
```

- Options: Flags that modify the behavior of curl.  
- URL: The URL of the server to which the request is being sent.  
- HTTP Methods
The -X flag is used to specify the HTTP method to be used for the request. For example:


```console
foo@bar:~$ curl -X GET http://example.com

foo@bar:~$ curl -X POST http://example.com
```

## Request Headers
The -H flag is used to specify request headers. For example:
foo


```console
foo@bar:~$ curl -H "Content-Type: application/json" http://example.com
```


## Request Body
The -d flag is used to specify the data to be sent in the request body.  
For example:


```console
foo@bar:~$ curl -X POST -H "Content-Type: application/json" -d '{"name": "John", "age": 30}' http://example.com
```
## Response Handling
By default, curl prints the response body to the terminal. The -o flag can be used to specify a file to write the response body to instead. For example:


```console
foo@bar:~$ curl -o response.json http://example.com/data.json
```
- The -i flag can be used to include the response headers in the output. For example:

```console
foo@bar:~$ curl -i http://example.com
```

- The -s flag can be used to silence all output from curl except for the response body. For example:

```console
foo@bar:~$ curl -s http://example.com
```

## Authentication
- The -u flag can be used to specify a username and password to use for authentication. For example:

```console
foo@bar:~$ curl -u username:password http://example.com
```

## SSL
- The -k flag can be used to allow insecure server connections when using SSL.   
For example:

```console
foo@bar:~$ curl -k https://example.com
```

## Redirects
- The -L flag can be used to follow redirects returned by the server.  
For example:

```console
curl -L http://example.com
```

---

This is a basic summary of curl usage. For more information, see the curl [documentation](https://curl.se/docs/).