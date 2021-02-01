# AppsDock Authentication Service

The AppsDock application server provides a build in authentication and authorization service to secure the resources. 
This topic provides an overview how to authenticate and access secured resources of the application server.

## Basics

The request of resources from AppsDock application server requires an access token from the AppsDock authentication
service. To obtain an access token, there must be a registered auth client at AppsDock identity management which must be 
used when requesting the auth endpoints with client credentials from your web or app application.

### Auth Client

The access of auth API endpoints requires at least one registered auth client at AppsDock identity management. 
The AppsDock identity management can register multiple auth client with different configurations which can be used by
different applications. Each auth client has its own credentials (client id or client id with secret) which must be used
when requesting the auth API. The credentials can be attached as basic base64 encoded Auhtorization header or as query
parameter at request uri.

### Access token

The access token is issued by the AppsDock authentication service and contains secured information (claims) about the
actual operator. The token also contains information which are used to validate/authenticate the operator and verify 
that it has the required permissions / is authorized to perform the operation. 
Access tokens have to be attached to each request that intents to access secured resources of the AppsDock application
server. The transport must be always over a secured channel like HTTPS.

An access token issued by the AppsDock authentication service looks like the following example:

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```

To attach the access token, you must set the access token as bearer type in the Authorization header.

## Authentication

The AppsDock authentication service provides an API for token and cookie based authentication management which 
includes the following operations:

Endpoint                | Operation
------------------------|---------------------------------------------------
/auth/token             | Authentication with email/username and password  
/auth/token/refresh     | Session/Token refresh via refresh token or cookie
/auth/revoke            | Revoke auth session via refresh token or cookie  

The AppsDock authentication service supports both token and cookie based authentication flows. 
 
### Token Based Auth
The token based authentication is used by confidential clients like mobile apps, which are capable of storing the 
refresh token securely. To obtain an access and refresh token, you have to send a request with the auth 
client credentials as authorization header to the token endpoint.

```
POST https://domain.com/auth/token
Content-Type: application/json
Authrorization: Basic WIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF

{"email": "jon@doe.com", "password": "xxxxx"}
```

The response contains the access/refresh token and additional information about the access token.

```json
{
    "expires_in": 180,
    "expires_at": 1595453215,
    "token_type": "bearer",
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0......",
    "refresh_token": "xwRJSMxNTE2MjMeKKF2QiwibmFtZSIfwpMeJf6Ik"
}
```

The access token must be attached as bearer token in Authorization header on each request of secured resources. 
The refresh token is used to refresh the access token when it expires and obtain a new access token.

!!! warning "Refresh token storage"
    The refresh token must be stored securely and should not be accessible by the client user. Do not store the refresh
    token into any kind of client side storages of web applications like local or session store nor into cookies.

### Cookie Based Auth

...... doc comming

```json
{
    "expires_in": 180,
    "expires_at": 1595453215
}
```

A cookie based client response only the expiry information about the current auth session, and uses an secured httpsonly
cookie to store the auth session information on client side. The auth cookie issued by the cookie based confidential client
has also a short lifetime like the access token, so it must be refreshed to keep the auth session valid.

!!! warning "Public clients"
    
    Public auth clients are currently not supported by the AppsDock authentication service!
    
## Refreshing

..