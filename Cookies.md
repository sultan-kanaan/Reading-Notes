## HTTP Cookies

An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to a user's web browser. The browser may store the cookie and send it back to the same server with later requests. 
Typically, an HTTP cookie is used to tell if two requests come from the same browser—keeping a user logged in, for example. It remembers stateful information for the stateless HTTP protocol.

>Cookies are mainly used for three purposes:

### Session management
Logins, shopping carts, game scores, or anything else the server should remember

### Personalization
User preferences, themes, and other settings

### Tracking
Recording and analyzing user behavior

## Creating cookies
After receiving an HTTP request, a server can send one or more Set-Cookie headers with the response. 
The browser usually stores the cookie and sends it with requests made to the same server inside a Cookie HTTP header. 

* You can specify an expiration date or time period after which the cookie shouldn't be sent. 

* You can also set additional restrictions to a specific domain and path to limit where the cookie is sent. 

The Set-Cookie HTTP response header sends cookies from the server to the user agent. A simple cookie is set like this:
```c#
Set-Cookie: <cookie-name>=<cookie-value>
```

This instructs the server sending headers to tell the client to store a pair of cookies:
```c#
HTTP/2.0 200 OK
Content-Type: text/html
Set-Cookie: yummy_cookie=choco
Set-Cookie: tasty_cookie=strawberry
[page content]
```
Then, with every subsequent request to the server, the browser sends all previously stored cookies back to the server using the Cookie header.

```c#
GET /sample_page.html HTTP/2.0
Host: www.example.org
Cookie: yummy_cookie=choco; tasty_cookie=strawberry
```


## Define the lifetime of a cookie
The lifetime of a cookie can be defined in two ways:

* Session cookies are deleted when the current session ends. The browser defines when the "current session" ends, and some browsers use session restoring when restarting. This can cause session cookies to last indefinitely.


* Permanent cookies are deleted at a date specified by the Expires attribute, or after a period of time specified by the Max-Age attribute.

## Restrict access to cookies

You can ensure that cookies are sent securely and aren't accessed by unintended parties or scripts in one of two ways: 

1. with the Secure attribute 
A cookie with the Secure attribute is only sent to the server with an encrypted request over the HTTPS protocol.
 It's never sent with unsecured HTTP (except on localhost), which means man-in-the-middle attackers can't access it easily. Insecure sites (with http: in the URL) can't set cookies with the Secure attribute. However, don't assume that Secure prevents all access to sensitive information in cookies. For example, someone with access to the client's hard disk (or JavaScript if the HttpOnly attribute isn't set) can read and modify the information.

2. the HttpOnly attribute
A cookie with the HttpOnly attribute is inaccessible to the JavaScript Document.cookie API; it's only sent to the server. For example, cookies that persist in server-side sessions don't need to be available to JavaScript and should have the HttpOnly attribute. This precaution helps mitigate cross-site scripting (XSS) attacks.


## Define where cookies are sent
### Domain attribute
The Domain attribute specifies which hosts can receive a cookie. If unspecified, the attribute defaults to the same host that set the cookie, excluding subdomains. If Domain is specified, then subdomains are always included. Therefore, specifying Domain is less restrictive than omitting it. However, it can be helpful when subdomains need to share information about a user.

For example, if you set Domain=mozilla.org, cookies are available on subdomains like developer.mozilla.org.

### Path attribute
The Path attribute indicates a URL path that must exist in the requested URL in order to send the Cookie header. The %x2F ("/") character is considered a directory separator, and subdirectories match as well.

For example, if you set Path=/docs, **these request paths match:**

/docs
/docs/
/docs/Web/
/docs/Web/HTTP

**But these request paths don't:**

/
/docsets
/fr/docs