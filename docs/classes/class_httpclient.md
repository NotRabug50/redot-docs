github\_url  
hide

# HTTPClient

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Low-level hyper-text transfer protocol client.

classref-introduction-group

## Description

Hyper-text transfer protocol client (sometimes called "User Agent").
Used to make HTTP requests to download web content, upload files and
other data or to communicate with various services, among other use
cases.

See the `HTTPRequest<class_HTTPRequest>` node for a higher-level
alternative.

\*\*Note:\*\* This client only needs to connect to a host once (see
`connect_to_host<class_HTTPClient_method_connect_to_host>`) to send
multiple requests. Because of this, methods that take URLs usually take
just the part after the host instead of the full URL, as the client is
already connected to a host. See
`request<class_HTTPClient_method_request>` for a full example and to get
started.

A **HTTPClient** should be reused between multiple requests or to
connect to different hosts instead of creating one client per request.
Supports Transport Layer Security (TLS), including server certificate
verification. HTTP status codes in the 2xx range indicate success, 3xx
redirection (i.e. "try again, but over here"), 4xx something was wrong
with the request, and 5xx something went wrong on the server's side.

For more information on HTTP, see [MDN's documentation on
HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP) (or read [RFC
2616](https://tools.ietf.org/html/rfc2616) to get it straight from the
source).

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

\*\*Note:\*\* It's recommended to use transport encryption (TLS) and to
avoid sending sensitive information (such as login credentials) in HTTP
GET URL parameters. Consider using HTTP POST requests or HTTP headers
for such information instead.

\*\*Note:\*\* When performing HTTP requests from a project exported to
Web, keep in mind the remote server may not allow requests from foreign
origins due to
[CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS). If you
host the server in question, you should modify its backend to allow
requests from foreign origins by adding the
`Access-Control-Allow-Origin: *` HTTP header.

\*\*Note:\*\* TLS support is currently limited to TLSv1.2 and TLSv1.3.
Attempting to connect to a server that only supports older (insecure)
TLS versions will return an error.

\*\*Warning:\*\* TLS certificate revocation and certificate pinning are
currently not supported. Revoked certificates are accepted as long as
they are otherwise valid. If this is a concern, you may want to use
automatically managed certificates with a short validity period.

classref-introduction-group

## Tutorials

-   `HTTP client class <../tutorials/networking/http_client_class>`
-   `TLS certificates <../tutorials/networking/ssl_certificates>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Method**: `🔗<enum_HTTPClient_Method>`

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_GET** = `0`

HTTP GET method. The GET method requests a representation of the
specified resource. Requests using GET should only retrieve data.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_HEAD** = `1`

HTTP HEAD method. The HEAD method asks for a response identical to that
of a GET request, but without the response body. This is useful to
request metadata like HTTP headers or to check if a resource exists.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_POST** = `2`

HTTP POST method. The POST method is used to submit an entity to the
specified resource, often causing a change in state or side effects on
the server. This is often used for forms and submitting data or
uploading files.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_PUT** = `3`

HTTP PUT method. The PUT method asks to replace all current
representations of the target resource with the request payload. (You
can think of POST as "create or update" and PUT as "update", although
many services tend to not make a clear distinction or change their
meaning).

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_DELETE** = `4`

HTTP DELETE method. The DELETE method requests to delete the specified
resource.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_OPTIONS** = `5`

HTTP OPTIONS method. The OPTIONS method asks for a description of the
communication options for the target resource. Rarely used.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_TRACE** = `6`

HTTP TRACE method. The TRACE method performs a message loop-back test
along the path to the target resource. Returns the entire HTTP request
received in the response body. Rarely used.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_CONNECT** = `7`

HTTP CONNECT method. The CONNECT method establishes a tunnel to the
server identified by the target resource. Rarely used.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_PATCH** = `8`

HTTP PATCH method. The PATCH method is used to apply partial
modifications to a resource.

classref-enumeration-constant

`Method<enum_HTTPClient_Method>` **METHOD\_MAX** = `9`

Represents the size of the `Method<enum_HTTPClient_Method>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Status**: `🔗<enum_HTTPClient_Status>`

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_DISCONNECTED** = `0`

Status: Disconnected from the server.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_RESOLVING** = `1`

Status: Currently resolving the hostname for the given URL into an IP.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_CANT\_RESOLVE** = `2`

Status: DNS failure: Can't resolve the hostname for the given URL.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_CONNECTING** = `3`

Status: Currently connecting to server.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_CANT\_CONNECT** = `4`

Status: Can't connect to the server.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_CONNECTED** = `5`

Status: Connection established.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_REQUESTING** = `6`

Status: Currently sending request.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_BODY** = `7`

Status: HTTP body received.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_CONNECTION\_ERROR** = `8`

Status: Error in HTTP connection.

classref-enumeration-constant

`Status<enum_HTTPClient_Status>` **STATUS\_TLS\_HANDSHAKE\_ERROR** = `9`

Status: Error in TLS handshake.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ResponseCode**: `🔗<enum_HTTPClient_ResponseCode>`

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_CONTINUE** =
`100`

HTTP status code `100 Continue`. Interim response that indicates
everything so far is OK and that the client should continue with the
request (or ignore this status if already finished).

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_SWITCHING\_PROTOCOLS** = `101`

HTTP status code `101 Switching Protocol`. Sent in response to an
`Upgrade` request header by the client. Indicates the protocol the
server is switching to.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_PROCESSING** =
`102`

HTTP status code `102 Processing` (WebDAV). Indicates that the server
has received and is processing the request, but no response is available
yet.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_OK** = `200`

HTTP status code `200 OK`. The request has succeeded. Default response
for successful requests. Meaning varies depending on the request. GET:
The resource has been fetched and is transmitted in the message body.
HEAD: The entity headers are in the message body. POST: The resource
describing the result of the action is transmitted in the message body.
TRACE: The message body contains the request message as received by the
server.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_CREATED** =
`201`

HTTP status code `201 Created`. The request has succeeded and a new
resource has been created as a result of it. This is typically the
response sent after a PUT request.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_ACCEPTED** =
`202`

HTTP status code `202 Accepted`. The request has been received but not
yet acted upon. It is non-committal, meaning that there is no way in
HTTP to later send an asynchronous response indicating the outcome of
processing the request. It is intended for cases where another process
or server handles the request, or for batch processing.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_NON\_AUTHORITATIVE\_INFORMATION** = `203`

HTTP status code `203 Non-Authoritative Information`. This response code
means returned meta-information set is not exact set as available from
the origin server, but collected from a local or a third party copy.
Except this condition, 200 OK response should be preferred instead of
this response.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_NO\_CONTENT** =
`204`

HTTP status code `204 No Content`. There is no content to send for this
request, but the headers may be useful. The user-agent may update its
cached headers for this resource with the new ones.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_RESET\_CONTENT** = `205`

HTTP status code `205 Reset Content`. The server has fulfilled the
request and desires that the client resets the "document view" that
caused the request to be sent to its original state as received from the
origin server.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_PARTIAL\_CONTENT** = `206`

HTTP status code `206 Partial Content`. This response code is used
because of a range header sent by the client to separate download into
multiple streams.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_MULTI\_STATUS**
= `207`

HTTP status code `207 Multi-Status` (WebDAV). A Multi-Status response
conveys information about multiple resources in situations where
multiple status codes might be appropriate.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_ALREADY\_REPORTED** = `208`

HTTP status code `208 Already Reported` (WebDAV). Used inside a DAV:
propstat response element to avoid enumerating the internal members of
multiple bindings to the same collection repeatedly.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_IM\_USED** =
`226`

HTTP status code `226 IM Used` (WebDAV). The server has fulfilled a GET
request for the resource, and the response is a representation of the
result of one or more instance-manipulations applied to the current
instance.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_MULTIPLE\_CHOICES** = `300`

HTTP status code `300 Multiple Choice`. The request has more than one
possible responses and there is no standardized way to choose one of the
responses. User-agent or user should choose one of them.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_MOVED\_PERMANENTLY** = `301`

HTTP status code `301 Moved Permanently`. Redirection. This response
code means the URI of requested resource has been changed. The new URI
is usually included in the response.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_FOUND** = `302`

HTTP status code `302 Found`. Temporary redirection. This response code
means the URI of requested resource has been changed temporarily. New
changes in the URI might be made in the future. Therefore, this same URI
should be used by the client in future requests.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_SEE\_OTHER** =
`303`

HTTP status code `303 See Other`. The server is redirecting the user
agent to a different resource, as indicated by a URI in the Location
header field, which is intended to provide an indirect response to the
original request.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_NOT\_MODIFIED**
= `304`

HTTP status code `304 Not Modified`. A conditional GET or HEAD request
has been received and would have resulted in a 200 OK response if it
were not for the fact that the condition evaluated to `false`.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_USE\_PROXY** =
`305`

**Deprecated:** Many clients ignore this response code for security
reasons. It is also deprecated by the HTTP standard.

HTTP status code `305 Use Proxy`.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_SWITCH\_PROXY**
= `306`

**Deprecated:** Many clients ignore this response code for security
reasons. It is also deprecated by the HTTP standard.

HTTP status code `306 Switch Proxy`.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_TEMPORARY\_REDIRECT** = `307`

HTTP status code `307 Temporary Redirect`. The target resource resides
temporarily under a different URI and the user agent MUST NOT change the
request method if it performs an automatic redirection to that URI.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_PERMANENT\_REDIRECT** = `308`

HTTP status code `308 Permanent Redirect`. The target resource has been
assigned a new permanent URI and any future references to this resource
ought to use one of the enclosed URIs.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_BAD\_REQUEST**
= `400`

HTTP status code `400 Bad Request`. The request was invalid. The server
cannot or will not process the request due to something that is
perceived to be a client error (e.g., malformed request syntax, invalid
request message framing, invalid request contents, or deceptive request
routing).

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_UNAUTHORIZED**
= `401`

HTTP status code `401 Unauthorized`. Credentials required. The request
has not been applied because it lacks valid authentication credentials
for the target resource.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_PAYMENT\_REQUIRED** = `402`

HTTP status code `402 Payment Required`. This response code is reserved
for future use. Initial aim for creating this code was using it for
digital payment systems, however this is not currently used.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_FORBIDDEN** =
`403`

HTTP status code `403 Forbidden`. The client does not have access rights
to the content, i.e. they are unauthorized, so server is rejecting to
give proper response. Unlike `401`, the client's identity is known to
the server.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_NOT\_FOUND** =
`404`

HTTP status code `404 Not Found`. The server can not find requested
resource. Either the URL is not recognized or the endpoint is valid but
the resource itself does not exist. May also be sent instead of 403 to
hide existence of a resource if the client is not authorized.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_METHOD\_NOT\_ALLOWED** = `405`

HTTP status code `405 Method Not Allowed`. The request's HTTP method is
known by the server but has been disabled and cannot be used. For
example, an API may forbid DELETE-ing a resource. The two mandatory
methods, GET and HEAD, must never be disabled and should not return this
error code.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_NOT\_ACCEPTABLE** = `406`

HTTP status code `406 Not Acceptable`. The target resource does not have
a current representation that would be acceptable to the user agent,
according to the proactive negotiation header fields received in the
request. Used when negotiation content.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_PROXY\_AUTHENTICATION\_REQUIRED** = `407`

HTTP status code `407 Proxy Authentication Required`. Similar to 401
Unauthorized, but it indicates that the client needs to authenticate
itself in order to use a proxy.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_REQUEST\_TIMEOUT** = `408`

HTTP status code `408 Request Timeout`. The server did not receive a
complete request message within the time that it was prepared to wait.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_CONFLICT** =
`409`

HTTP status code `409 Conflict`. The request could not be completed due
to a conflict with the current state of the target resource. This code
is used in situations where the user might be able to resolve the
conflict and resubmit the request.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_GONE** = `410`

HTTP status code `410 Gone`. The target resource is no longer available
at the origin server and this condition is likely permanent.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_LENGTH\_REQUIRED** = `411`

HTTP status code `411 Length Required`. The server refuses to accept the
request without a defined Content-Length header.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_PRECONDITION\_FAILED** = `412`

HTTP status code `412 Precondition Failed`. One or more conditions given
in the request header fields evaluated to `false` when tested on the
server.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_REQUEST\_ENTITY\_TOO\_LARGE** = `413`

HTTP status code `413 Entity Too Large`. The server is refusing to
process a request because the request payload is larger than the server
is willing or able to process.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_REQUEST\_URI\_TOO\_LONG** = `414`

HTTP status code `414 Request-URI Too Long`. The server is refusing to
service the request because the request-target is longer than the server
is willing to interpret.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_UNSUPPORTED\_MEDIA\_TYPE** = `415`

HTTP status code `415 Unsupported Media Type`. The origin server is
refusing to service the request because the payload is in a format not
supported by this method on the target resource.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_REQUESTED\_RANGE\_NOT\_SATISFIABLE** = `416`

HTTP status code `416 Requested Range Not Satisfiable`. None of the
ranges in the request's Range header field overlap the current extent of
the selected resource or the set of ranges requested has been rejected
due to invalid ranges or an excessive request of small or overlapping
ranges.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_EXPECTATION\_FAILED** = `417`

HTTP status code `417 Expectation Failed`. The expectation given in the
request's Expect header field could not be met by at least one of the
inbound servers.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_IM\_A\_TEAPOT**
= `418`

HTTP status code `418 I'm A Teapot`. Any attempt to brew coffee with a
teapot should result in the error code "418 I'm a teapot". The resulting
entity body MAY be short and stout.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_MISDIRECTED\_REQUEST** = `421`

HTTP status code `421 Misdirected Request`. The request was directed at
a server that is not able to produce a response. This can be sent by a
server that is not configured to produce responses for the combination
of scheme and authority that are included in the request URI.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_UNPROCESSABLE\_ENTITY** = `422`

HTTP status code `422 Unprocessable Entity` (WebDAV). The server
understands the content type of the request entity (hence a 415
Unsupported Media Type status code is inappropriate), and the syntax of
the request entity is correct (thus a 400 Bad Request status code is
inappropriate) but was unable to process the contained instructions.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_LOCKED** =
`423`

HTTP status code `423 Locked` (WebDAV). The source or destination
resource of a method is locked.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_FAILED\_DEPENDENCY** = `424`

HTTP status code `424 Failed Dependency` (WebDAV). The method could not
be performed on the resource because the requested action depended on
another action and that action failed.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_UPGRADE\_REQUIRED** = `426`

HTTP status code `426 Upgrade Required`. The server refuses to perform
the request using the current protocol but might be willing to do so
after the client upgrades to a different protocol.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_PRECONDITION\_REQUIRED** = `428`

HTTP status code `428 Precondition Required`. The origin server requires
the request to be conditional.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_TOO\_MANY\_REQUESTS** = `429`

HTTP status code `429 Too Many Requests`. The user has sent too many
requests in a given amount of time (see "rate limiting"). Back off and
increase time between requests or try again later.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_REQUEST\_HEADER\_FIELDS\_TOO\_LARGE** = `431`

HTTP status code `431 Request Header Fields Too Large`. The server is
unwilling to process the request because its header fields are too
large. The request MAY be resubmitted after reducing the size of the
request header fields.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_UNAVAILABLE\_FOR\_LEGAL\_REASONS** = `451`

HTTP status code `451 Response Unavailable For Legal Reasons`. The
server is denying access to the resource as a consequence of a legal
demand.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_INTERNAL\_SERVER\_ERROR** = `500`

HTTP status code `500 Internal Server Error`. The server encountered an
unexpected condition that prevented it from fulfilling the request.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_NOT\_IMPLEMENTED** = `501`

HTTP status code `501 Not Implemented`. The server does not support the
functionality required to fulfill the request.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_BAD\_GATEWAY**
= `502`

HTTP status code `502 Bad Gateway`. The server, while acting as a
gateway or proxy, received an invalid response from an inbound server it
accessed while attempting to fulfill the request. Usually returned by
load balancers or proxies.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_SERVICE\_UNAVAILABLE** = `503`

HTTP status code `503 Service Unavailable`. The server is currently
unable to handle the request due to a temporary overload or scheduled
maintenance, which will likely be alleviated after some delay. Try again
later.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_GATEWAY\_TIMEOUT** = `504`

HTTP status code `504 Gateway Timeout`. The server, while acting as a
gateway or proxy, did not receive a timely response from an upstream
server it needed to access in order to complete the request. Usually
returned by load balancers or proxies.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_HTTP\_VERSION\_NOT\_SUPPORTED** = `505`

HTTP status code `505 HTTP Version Not Supported`. The server does not
support, or refuses to support, the major version of HTTP that was used
in the request message.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_VARIANT\_ALSO\_NEGOTIATES** = `506`

HTTP status code `506 Variant Also Negotiates`. The server has an
internal configuration error: the chosen variant resource is configured
to engage in transparent content negotiation itself, and is therefore
not a proper end point in the negotiation process.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_INSUFFICIENT\_STORAGE** = `507`

HTTP status code `507 Insufficient Storage`. The method could not be
performed on the resource because the server is unable to store the
representation needed to successfully complete the request.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_LOOP\_DETECTED** = `508`

HTTP status code `508 Loop Detected`. The server terminated an operation
because it encountered an infinite loop while processing a request with
"Depth: infinity". This status indicates that the entire operation
failed.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>` **RESPONSE\_NOT\_EXTENDED**
= `510`

HTTP status code `510 Not Extended`. The policy for accessing the
resource has not been met in the request. The server should send back
all the information necessary for the client to issue an extended
request.

classref-enumeration-constant

`ResponseCode<enum_HTTPClient_ResponseCode>`
**RESPONSE\_NETWORK\_AUTH\_REQUIRED** = `511`

HTTP status code `511 Network Authentication Required`. The client needs
to authenticate to gain network access.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **blocking\_mode\_enabled** = `false`
`🔗<class_HTTPClient_property_blocking_mode_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_blocking\_mode**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_blocking\_mode\_enabled**()

If `true`, execution will block until all data is read from the
response.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StreamPeer<class_StreamPeer>` **connection**
`🔗<class_HTTPClient_property_connection>`

classref-property-setget

-   `void (No return value.)` **set\_connection**(value:
    `StreamPeer<class_StreamPeer>`)
-   `StreamPeer<class_StreamPeer>` **get\_connection**()

The connection to use for this client.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **read\_chunk\_size** = `65536`
`🔗<class_HTTPClient_property_read_chunk_size>`

classref-property-setget

-   `void (No return value.)` **set\_read\_chunk\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_read\_chunk\_size**()

The size of the buffer used and maximum bytes to read per iteration. See
`read_response_body_chunk<class_HTTPClient_method_read_response_body_chunk>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **close**()
`🔗<class_HTTPClient_method_close>`

Closes the current connection, allowing reuse of this **HTTPClient**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_to\_host**(host:
`String<class_String>`, port: `int<class_int>` = -1, tls\_options:
`TLSOptions<class_TLSOptions>` = null)
`🔗<class_HTTPClient_method_connect_to_host>`

Connects to a host. This needs to be done before any requests are sent.

If no `port` is specified (or `-1` is used), it is automatically set to
80 for HTTP and 443 for HTTPS. You can pass the optional `tls_options`
parameter to customize the trusted certification authorities, or the
common name verification when using HTTPS. See
`TLSOptions.client<class_TLSOptions_method_client>` and
`TLSOptions.client_unsafe<class_TLSOptions_method_client_unsafe>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_response\_body\_length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_HTTPClient_method_get_response_body_length>`

Returns the response's body length.

\*\*Note:\*\* Some Web servers may not send a body length. In this case,
the value returned will be `-1`. If using chunked transfer encoding, the
body length will also be `-1`.

\*\*Note:\*\* This function always returns `-1` on the Web platform due
to browsers limitations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_response\_code**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_HTTPClient_method_get_response_code>`

Returns the response's HTTP status code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_response\_headers**()
`🔗<class_HTTPClient_method_get_response_headers>`

Returns the response headers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**get\_response\_headers\_as\_dictionary**()
`🔗<class_HTTPClient_method_get_response_headers_as_dictionary>`

Returns all response headers as a `Dictionary<class_Dictionary>`. Each
entry is composed by the header name, and a `String<class_String>`
containing the values separated by `"; "`. The casing is kept the same
as the headers were received.

    {
        "content-length": 12,
        "Content-Type": "application/json; charset=UTF-8",
    }

classref-item-separator

------------------------------------------------------------------------

classref-method

`Status<enum_HTTPClient_Status>` **get\_status**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_HTTPClient_method_get_status>`

Returns a `Status<enum_HTTPClient_Status>` constant. Need to call
`poll<class_HTTPClient_method_poll>` in order to get status updates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_response**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_HTTPClient_method_has_response>`

If `true`, this **HTTPClient** has a response available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_response\_chunked**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_HTTPClient_method_is_response_chunked>`

If `true`, this **HTTPClient** has a response that is chunked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **poll**()
`🔗<class_HTTPClient_method_poll>`

This needs to be called in order to have any request processed. Check
results with `get_status<class_HTTPClient_method_get_status>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **query\_string\_from\_dict**(fields:
`Dictionary<class_Dictionary>`)
`🔗<class_HTTPClient_method_query_string_from_dict>`

Generates a GET/POST application/x-www-form-urlencoded style query
string from a provided dictionary, e.g.:

gdscript

var fields = {"username": "user", "password": "pass"} var query\_string
= http\_client.query\_string\_from\_dict(fields) \# Returns
"username=user&password=pass"

csharp

var fields = new Godot.Collections.Dictionary { { "username", "user" },
{ "password", "pass" } }; string queryString =
httpClient.QueryStringFromDict(fields); // Returns
"username=user&password=pass"

Furthermore, if a key has a `null` value, only the key itself is added,
without equal sign and value. If the value is an array, for each value
in it a pair with the same key is added.

gdscript

var fields = {"single": 123, "not\_valued": null, "multiple": \[22, 33,
44\]} var query\_string = http\_client.query\_string\_from\_dict(fields)
\# Returns "single=123&not\_valued&multiple=22&multiple=33&multiple=44"

csharp

var fields = new Godot.Collections.Dictionary { { "single", 123 }, {
"notValued", default }, { "multiple", new Godot.Collections.Array { 22,
33, 44 } }, }; string queryString =
httpClient.QueryStringFromDict(fields); // Returns
"single=123&not\_valued&multiple=22&multiple=33&multiple=44"

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**read\_response\_body\_chunk**()
`🔗<class_HTTPClient_method_read_response_body_chunk>`

Reads one chunk from the response.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **request**(method:
`Method<enum_HTTPClient_Method>`, url: `String<class_String>`, headers:
`PackedStringArray<class_PackedStringArray>`, body:
`String<class_String>` = "") `🔗<class_HTTPClient_method_request>`

Sends a request to the connected host.

The URL parameter is usually just the part after the host, so for
`https://somehost.com/index.php`, it is `/index.php`. When sending
requests to an HTTP proxy server, it should be an absolute URL. For
`METHOD_OPTIONS<class_HTTPClient_constant_METHOD_OPTIONS>` requests, `*`
is also allowed. For
`METHOD_CONNECT<class_HTTPClient_constant_METHOD_CONNECT>` requests, it
should be the authority component (`host:port`).

Headers are HTTP request headers. For available HTTP methods, see
`Method<enum_HTTPClient_Method>`.

To create a POST request with query strings to push to the server, do:

gdscript

var fields = {"username" : "user", "password" : "pass"} var
query\_string = http\_client.query\_string\_from\_dict(fields) var
headers = \["Content-Type: application/x-www-form-urlencoded",
"Content-Length: " + str(query\_string.length())\] var result =
http\_client.request(http\_client.METHOD\_POST, "/index.php", headers,
query\_string)

csharp

var fields = new Godot.Collections.Dictionary { { "username", "user" },
{ "password", "pass" } }; string queryString = new
HttpClient().QueryStringFromDict(fields); string\[\] headers = {
"Content-Type: application/x-www-form-urlencoded", $"Content-Length:
{queryString.Length}" }; var result = new
HttpClient().Request(HttpClient.Method.Post, "index.php", headers,
queryString);

\*\*Note:\*\* The `body` parameter is ignored if `method` is
`METHOD_GET<class_HTTPClient_constant_METHOD_GET>`. This is because GET
methods can't contain request data. As a workaround, you can pass
request data as a query string in the URL. See
`String.uri_encode<class_String_method_uri_encode>` for an example.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **request\_raw**(method:
`Method<enum_HTTPClient_Method>`, url: `String<class_String>`, headers:
`PackedStringArray<class_PackedStringArray>`, body:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_HTTPClient_method_request_raw>`

Sends a raw request to the connected host.

The URL parameter is usually just the part after the host, so for
`https://somehost.com/index.php`, it is `/index.php`. When sending
requests to an HTTP proxy server, it should be an absolute URL. For
`METHOD_OPTIONS<class_HTTPClient_constant_METHOD_OPTIONS>` requests, `*`
is also allowed. For
`METHOD_CONNECT<class_HTTPClient_constant_METHOD_CONNECT>` requests, it
should be the authority component (`host:port`).

Headers are HTTP request headers. For available HTTP methods, see
`Method<enum_HTTPClient_Method>`.

Sends the body data raw, as a byte array and does not encode it in any
way.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_http\_proxy**(host:
`String<class_String>`, port: `int<class_int>`)
`🔗<class_HTTPClient_method_set_http_proxy>`

Sets the proxy server for HTTP requests.

The proxy server is unset if `host` is empty or `port` is -1.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_https\_proxy**(host:
`String<class_String>`, port: `int<class_int>`)
`🔗<class_HTTPClient_method_set_https_proxy>`

Sets the proxy server for HTTPS requests.

The proxy server is unset if `host` is empty or `port` is -1.
