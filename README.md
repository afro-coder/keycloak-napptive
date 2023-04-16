# Keycloak

Keycloak is an Open Source Identity and Access Management solution for modern Applications and Services.

### Check the deployment
#### Pre-requisites:
- Playground CLI installed & logged in
 - Check the [documentation](https://docs.napptive.com/playground/CLI.html)

Deploy this application from the CLI:
```
playground apps deploy https://github.com/afro-coder/keycloak-napptive
```

Or simply download the zip from Github and upload it to the Napptive UI

Once the application is deployed you can see the status in the Napptive UI

If you use the CLI once the application is deployed from the Catalog you can use the following command.

```
playground apps info keycloak-server
```

Output should be similar to:
```
Target environment: mediocredevops/default
NAME               STATUS
keycloak-server    RUNNING

COMPONENT             STATUS     SCOPES    TRAITS
keycloak-container    RUNNING              resource, scaler, napptive-ingress

COMPONENT             INGRESSES
keycloak-container    keycloak-ui-<random-id>.apps.playground.napptive.dev
```

Logs for the deployment can be viewed by
```
playground apps logs keycloak-server
```

### Access the UI
- Navigate to your ingress URL, you should be able to see this in the napptive playground.
![Napptive UI showing the endpoint](https://i.imgur.com/olfNrJW.png)
- Use `admin` and `admin123` for both username and password to login. Please make sure to change these after the first login.

![Keycloak Admin Server](https://i.imgur.com/cFu3TU7.png)

*Note*: This is not a Production ready keycloak environment, to switch to production you need to issue TLS certs and a lot more please look at the [documentation](https://www.keycloak.org/server/configuration-production)

This is a minimal Development setup, which is stateless, please use this for demo/testing.

