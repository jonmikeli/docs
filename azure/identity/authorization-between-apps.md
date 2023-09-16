# How to implement authorization mechanisms between applications with Azure AD

This publication describes how to implement security mechanisms (authorization):
 - between two applications
 - without relying on user authentication
 - without using Managed Identities


# Problem to solve

The typical scenario in mind is:
 - front application
 - API or gateway
 - how to implement a security mechanism to be sure that the API or gateway can only be called by the front application

# How

These are the steps to follow in order to implement the solution:
 - register the front application at AAD B2C
 - register the gateway application at AAD B2C
 - update gateway application "appRoles" at AAD B2C with applicative roles below

```json
"appRoles": [
{
  "allowedMemberTypes": ["Application"],
  "displayName": "Read",
  "id": "d6a15e20-f83c-4264-8e61-5082688e14c8",
  "isEnabled": true,
  "description": "Readers have the ability to read tasks.",
  "value": "app.read"
},
{
  "allowedMemberTypes": ["Application"],
  "displayName": "Write",
  "id": "204dc4ab-51e1-439f-8c7f-31a1ebf3c7b9",
  "isEnabled": true,
  "description": "Writers have the ability to create tasks.",
  "value": "app.write"
}]
```

> NOTE
>
> The previous settings are not available through the UI in the portal. You will need to update the json directly (can be done through the manifest editor in the portal).

This setting is needed to be able to configure permissions regarding the access to the app and its scopes, as an application and not in a delegated manner.

 - create the API ID at AAD B2C
 - configure API permissions at front application level
  
 - configure tenant Id, client Id, client secret (front) and the requested API scope at front application level
 - configure tenant Id, client Id, client secret (gateway)
  
 - implement and inject security features at both applicatons

 - add user oriented flows and policies at front level and AAD B2C
 - configure them at front application level


> NOTE
>
> The implemented POC does not implement VNET and private endpoints.
> It focuses on AAD B2C, front and gateway applications with their settings.

# Sources

References:
 - [GitHub repo with some samples](https://github.com/Azure-Samples/ms-identity-blazor-server/blob/main/WebApp-your-API/B2C/README-Incremental.md)
 - [Daemon application registration](https://learn.microsoft.com/en-us/azure/active-directory-b2c/client-credentials-grant-flow?pivots=b2c-user-flow) (daemon apps registration with full details)