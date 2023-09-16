# How to register an application in a different tenant

Problem: register an application in a different tenant than the one you are logged in.
Why: this is quite common in development steps or when the solution uses more than one tenant.

# How to


 - log to the target tenant using the following command:

```bash
az login --allow-no-subscriptions
```
With this command you will be able to see the tenant you need to register the application in.

 - set the target tenant using the following command:

```bash
az account set -s [id]
```

 - register the application 


# References

 - [Documentation](https://elischei.com/how-to-register-an-application-in-azure-ad-using-azure-cli/)