# Read:33 Summary
## JSON Web Tokens
* JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. 
This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private
key pair using RSA or ECDSA.
* Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims 
contained within it, while encrypted tokens hide those claims from other parties. When tokens are signed using public/private key pairs, the signature 
also certifies that only the party holding the private key is the one that signed it.
### When should you use JSON Web Tokens?
  * `Authorization`: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access 
routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

  * `Information Exchange`: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private
key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that
the content hasn't been tampered with.
### What is the JSON Web Token structure?
* In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

  * Header
  * Payload
  * Signature
### How do JSON Web Tokens work?
* In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care
must be taken to prevent security issues. In general, you should not keep tokens longer than required.
* You also should not store sensitive session data in browser storage due to lack of security.

* Whenever the user wants to access a protected route or resource, the user agent should send the JWT, typically in the Authorization header using the Bearer schema.
### how a JWT is obtained and used to access APIs or resources:
* The application or client requests authorization to the authorization server. This is performed through one of the different authorization flows. For example, a
typical OpenID Connect compliant web application will go through the /oauth/authorize endpoint using the authorization code flow.
* When the authorization is granted, the authorization server returns an access token to the application.
* The application uses the access token to access a protected resource (like an API).

***Do note that with signed tokens, all the information contained within the token is exposed to users or other parties, even though they are unable to change it. 
This means you should not put secret information within the token.***

### Why should we use JSON Web Tokens?
* As JSON is less verbose than XML, when it is encoded its size is also smaller, making JWT more compact than SAML. This makes JWT a good choice to be passed 
in HTML and HTTP environments.
* Security-wise, SWT can only be symmetrically signed by a shared secret using the HMAC algorithm. However, JWT and SAML tokens can use a public/private key
pair in the form of a X.509 certificate for signing. Signing XML with XML Digital Signature without introducing obscure security holes is very difficult when 
compared to the simplicity of signing JSON.
* JSON parsers are common in most programming languages because they map directly to objects. Conversely, XML doesn't have a natural document-to-object mapping. 
This makes it easier to work with JWT than SAML assertions.
* Regarding usage, JWT is used at Internet scale. This highlights the ease of client-side processing of the JSON Web token on multiple platforms, especially mobile.






