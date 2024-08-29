# 1xx Informational Responses<br>
100 Continue: The initial part of the request has been received and has not yet been rejected by the server.<br>
101 Switching Protocols: The server is switching protocols according to the request.<br>

# 2xx Success<br>
200 OK: The request was successful, and the response contains the requested data.<br>
201 Created: The request was successful, and a new resource was created.<br>
202 Accepted: The request has been accepted for processing, but the processing is not yet complete.<br>
203 Non-Authoritative Information: The request was successful, but the information returned may be from a local or third-party copy.<br>
204 No Content: The request was successful, but there is no content to send in the response.<br>
205 Reset Content: The request was successful, and the user agent should reset the document view.<br>
206 Partial Content: The server is delivering only part of the resource due to a range header sent by the client.<br>

# 3xx Redirection<br>
300 Multiple Choices: The request has more than one possible responses.<br>
301 Moved Permanently: The resource has been moved to a new URI permanently.<br>
302 Found: The resource is temporarily located at a different URI.<br>
303 See Other: The response to the request can be found under a different URI using a GET method.<br>
304 Not Modified: The resource has not been modified since the last request.<br>
305 Use Proxy: The requested resource must be accessed through a proxy.<br>
306 Switch Proxy: No longer used. Originally meant to indicate a subsequent request should use the specified proxy.<br>
307 Temporary Redirect: The resource resides temporarily at a different URI.<br>
308 Permanent Redirect: The resource has been moved permanently to a new URI.<br>

# 4xx Client Errors<br>
400 Bad Request: The request was invalid or cannot be processed.<br>
401 Unauthorized: Authentication is required or has failed.<br>
402 Payment Required: Reserved for future use. Initially intended for digital payment systems.<br>
403 Forbidden: The request is understood but refused.<br>
404 Not Found: The requested resource was not found.<br>
405 Method Not Allowed: The method used is not allowed for the requested resource.<br>
406 Not Acceptable: The resource is only capable of generating content not acceptable according to the Accept headers sent in the request.<br>
407 Proxy Authentication Required: Authentication with a proxy is required.<br>
408 Request Timeout: The server timed out waiting for the request.<br>
409 Conflict: The request could not be completed due to a conflict with the current state of the resource.<br>
410 Gone: The resource requested is no longer available and will not be available again.<br>
411 Length Required: The request did not specify the length of its content, which is required by the server.<br>
412 Precondition Failed: One or more conditions in the request header fields evaluated to false.<br>
413 Payload Too Large: The request is larger than the server is willing or able to process.<br>
414 URI Too Long: The URI provided was too long for the server to process.<br>
415 Unsupported Media Type: The request entity has a media type which the server or resource does not support.<br>
416 Range Not Satisfiable: The server cannot provide the requested portion of the resource.<br>
417 Expectation Failed: The server cannot meet the requirements of the Expect request-header field.<br>
418 I'm a teapot: An April Fools' joke from RFC 2324. The server is a teapot and cannot brew coffee.<br>

# 5xx Server Errors<br>
500 Internal Server Error: An error occurred on the server.<br>
501 Not Implemented: The server does not support the functionality required to fulfill the request.<br>
502 Bad Gateway: The server received an invalid response from the upstream server.<br>
503 Service Unavailable: The server is currently unable to handle the request due to temporary overloading or maintenance.<br>
504 Gateway Timeout: The server did not receive a timely response from an upstream server or some other auxiliary server.<br>
505 HTTP Version Not Supported: The server does not support the HTTP protocol version that was used in the request.<br>
506 Variant Also Negotiates: The server has an internal configuration error: transparent content negotiation for the request results in a circular reference.<br>
507 Insufficient Storage: The server is unable to store the representation needed to complete the request.<br>
508 Loop Detected: The server detected an infinite loop while processing a request.<br>
510 Not Extended: Further extensions to the request are required for the server to fulfill it.<br>

# 6xx Unofficial Extensions<br>
600 Unparseable Response Headers: This is not a standard status code and is used by some servers to indicate that response headers could not be parsed.<br>
