---
layout: post
title:      "JSON Web Tokens (JWT)"
date:       2018-06-26 03:04:12 +0000
permalink:  json_web_tokens_jwt
---


One way to enable an authentication feature on a react/redux frontend is to use JWT.

JWT is a compact and self-contained way for securely transmitting information between parties as a JSON object.  The information in the JSON object (aka JWT) can be verified and trusted because it is digitally signed.  The information can also be encrypted to provide secrecy between parties.

For authorization purposes, an encrypted token is created once the user is logged in, and each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. 

Most of the time, JWT is used for a Single Sign On feature because of its small overhead and its ability to be easily used across different domains.

#Structure

In its compact form, JWT consists of three parts separated by dots (.), which are:

Header
Payload
Signature

Therefore, a JWT typically looks like the following.

```
xxxxx.yyyyy.zzzzz
```

1. At a minimum, **Header** consists of two parts: the type of the token/signature and the hashing/encryption algorithm being used, such as HMAC SHA256 or RSA. 
The header may also contain metadata for the JWT.

For example:

```
{
  "alg": "HS256",
  "typ": "JWT"
}
```

2. **Payload** contains the claims, which are statements about an entity (typically, the user) and additional data -- *encrypted* if used for authorization purposes. 

For example:

```
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```


3. **Signature** part is created when the headers and payloads are digitally signed using the algorithm specified in the header.

The signature is used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify that the sender of the JWT is who it says it is.


If you want to play with JWT and put these concepts into practice, you can use[ jwt.io](http:// jwt.io) Debugger to decode, verify, and generate JWTs.





