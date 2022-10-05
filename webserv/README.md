# webserv (42 Project)

This project is about writing a static HTTP server with c++98.

## Intro:

The primary function of a web server is to store, process and deliver web pages to clients using HTTP.
To use a web server, the client need to send HTTP request (with browser for example), the server find the requested document and send HTTP response with the document needed by the client.

---

## HTTP:

HTTP ([Hypertext Transfer Protocol](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)) is an application layer protocol used for access others ressources with [hyperlink](https://en.wikipedia.org/wiki/Hyperlink) easily, for exemple by a mouse click.

### HTTP Request

HTTP request method needed in webserv:
- GET: Request a ressource from the server.
- POST: Send data to the server.
- DELETE: Delete a ressource from the server.

Exemple:
```http
GET / HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-GB,en;q=0.5
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

### HTTP Response

HTTP response status code:
- 1XX: The request was received, continuing process.
- 2XX: The request was successfully received, understood and accepted.
- 3XX: Further action needs to be taken in order to complete the request.
- 4XX: The request contains bad syntax or cannot be fulfilled.
- 5XX: The server failed to fulfill an apparently valid request.

Exemple:
```http
HTTP/1.1 200 OK
Date: Mon, 23 May 2005 22:38:34 GMT
Content-Type: text/html; charset=UTF-8
Content-Length: 155
Last-Modified: Wed, 08 Jan 2003 23:11:55 GMT
Server: Apache/1.3.3.7 (Unix) (Red-Hat/Linux)
ETag: "3f80f-1b6-3e1cb03b"
Accept-Ranges: bytes
Connection: close

<html>
  <head>
    <title>An Example Page</title>
  </head>
  <body>
    <p>Hello World, this is a very simple HTML document.</p>
  </body>
</html>
```
