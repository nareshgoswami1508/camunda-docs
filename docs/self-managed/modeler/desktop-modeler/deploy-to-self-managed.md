---
id: deploy-to-self-managed
title: Deploy diagram
description: "Desktop Modeler can directly deploy diagrams and start process instances in Camunda 8 Self-Managed."
---

Desktop Modeler can directly deploy diagrams and start process instances in Camunda 8 Self-Managed. Follow the steps below to deploy a diagram:

1. Click the rocket-shaped deployment icon:

![deployment icon](./img/deploy-icon.png)

2. Click **Camunda 8 Self-Managed**:

![deployment configuration](./img/deploy-empty.png)

3. Input the `Cluster endpoint`:

:::note
You can connect to Camunda 8 both securely and insecurely through the `https` and `http` protocols.

Secured connections to a remote endpoint will only be established if the remote server certificate is trusted by the app. Ensure that signing trusted roots and intermediate certificates [are known to the app](/components/modeler/desktop-modeler/flags/flags.md#zeebe-ssl-certificate).
:::

![deployment via Camunda 8](./img/deploy-endpoint.png)

4. Select **OAuth**, and input the credentials in case your gateway requires authentication:

:::note
The OAuth URL needs to contain the full path to the token endpoint, i.e. `https://<keycloak base url>/auth/realms/camunda-platform/protocol/openid-connect/token`.
:::

![oauth configuration](./img/deploy-with-oauth.png)

5. Select the **Remember** checkbox if you want to locally store the connection information.

6. Click **Deploy** to perform the actual deployment.

![deployment successful](./img/deploy-success.png)
