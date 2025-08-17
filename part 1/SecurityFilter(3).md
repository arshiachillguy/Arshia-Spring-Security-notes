# security filters in java (with a Focus on spring security ) 

In Java web applications, security filters are components that intercept HTTP requests and enforce security rules (authentication, authorization, headers, etc.) before they reach your application logic. They form the backbone of frameworks like Spring Security.

## What is a security filter?

`javax.servlet.Filter`: that inspects/modifies requests responses.  
That used for:  
- Authentication (login, JWT validation)  
- Authorization (role/permission checks)  
- Headers (CORS, CSRF protection)  
- Logging/auditing  

## Key security filters in spring security

| Filter Class | Purpose |
|--------------|---------|
| `SecurityContextPersistenceFilter` | Restore SecurityContext |
| `UsernamePasswordAuthenticationFilter` | Process form-based login |
| `BasicAuthenticationFilter` | Handle HTTP Basic Auth |
| `BearerTokenAuthenticationFilter` | Validates OAuth2/JWT tokens |
| `AnonymousAuthenticationFilter` | Assigns a default anonymous user if no auth is found |
| `CsrfFilter` | Protect against Cross-site Request Forgery attacks |
| `AuthorizationFilter` | Checks permissions |

## How filters work in spring security?

1. Request enters the filter chain  
2. Each filter checks/modifies the request  
3. If a filter blocks the request: returns 401 or 403 error  
4. If all filters pass: request reaches your `@RestController`  
