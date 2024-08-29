-#1xx Informational Responses
100 Continue: The initial part of the request has been received and has not yet been rejected by the server.
101 Switching Protocols: The server is switching protocols according to the request.
-#2xx Success
200 OK: The request was successful, and the response contains the requested data.
201 Created: The request was successful, and a new resource was created.
202 Accepted: The request has been accepted for processing, but the processing is not yet complete.
203 Non-Authoritative Information: The request was successful, but the information returned may be from a local or third-party copy.
204 No Content: The request was successful, but there is no content to send in the response.
205 Reset Content: The request was successful, and the user agent should reset the document view.
206 Partial Content: The server is delivering only part of the resource due to a range header sent by the client.
-#3xx Redirection
300 Multiple Choices: The request has more than one possible responses.
301 Moved Permanently: The resource has been moved to a new URI permanently.
302 Found: The resource is temporarily located at a different URI.
303 See Other: The response to the request can be found under a different URI using a GET method.
304 Not Modified: The resource has not been modified since the last request.
305 Use Proxy: The requested resource must be accessed through a proxy.
306 Switch Proxy: No longer used. Originally meant to indicate a subsequent request should use the specified proxy.
307 Temporary Redirect: The resource resides temporarily at a different URI.
308 Permanent Redirect: The resource has been moved permanently to a new URI.
-#4xx Client Errors
400 Bad Request: The request was invalid or cannot be processed.
401 Unauthorized: Authentication is required or has failed.
402 Payment Required: Reserved for future use. Initially intended for digital payment systems.
403 Forbidden: The request is understood but refused.
404 Not Found: The requested resource was not found.
405 Method Not Allowed: The method used is not allowed for the requested resource.
406 Not Acceptable: The resource is only capable of generating content not acceptable according to the Accept headers sent in the request.
407 Proxy Authentication Required: Authentication with a proxy is required.
408 Request Timeout: The server timed out waiting for the request.
409 Conflict: The request could not be completed due to a conflict with the current state of the resource.
410 Gone: The resource requested is no longer available and will not be available again.
411 Length Required: The request did not specify the length of its content, which is required by the server.
412 Precondition Failed: One or more conditions in the request header fields evaluated to false.
413 Payload Too Large: The request is larger than the server is willing or able to process.
414 URI Too Long: The URI provided was too long for the server to process.
415 Unsupported Media Type: The request entity has a media type which the server or resource does not support.
416 Range Not Satisfiable: The server cannot provide the requested portion of the resource.
417 Expectation Failed: The server cannot meet the requirements of the Expect request-header field.
418 I'm a teapot: An April Fools' joke from RFC 2324. The server is a teapot and cannot brew coffee.
-#5xx Server Errors
500 Internal Server Error: An error occurred on the server.
501 Not Implemented: The server does not support the functionality required to fulfill the request.
502 Bad Gateway: The server received an invalid response from the upstream server.
503 Service Unavailable: The server is currently unable to handle the request due to temporary overloading or maintenance.
504 Gateway Timeout: The server did not receive a timely response from an upstream server or some other auxiliary server.
505 HTTP Version Not Supported: The server does not support the HTTP protocol version that was used in the request.
506 Variant Also Negotiates: The server has an internal configuration error: transparent content negotiation for the request results in a circular reference.
507 Insufficient Storage: The server is unable to store the representation needed to complete the request.
508 Loop Detected: The server detected an infinite loop while processing a request.
510 Not Extended: Further extensions to the request are required for the server to fulfill it.
-#6xx Unofficial Extensions
600 Unparseable Response Headers: This is not a standard status code and is used by some servers to indicate that response headers could not be parsed.
