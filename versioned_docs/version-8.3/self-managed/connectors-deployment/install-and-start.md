---
id: install-and-start
title: Installation
description: "Let's get started with Connectors by installing and running them."
---

The concept of a [Connector](/components/connectors/introduction.md) consists of two parts:

- The business logic is implemented by a [Connector function](/components/connectors/custom-built-connectors/connector-sdk.md#runtime-logic)
  and executed by a [Connector runtime environment](/components/connectors/custom-built-connectors/connector-sdk.md#runtime-environments).
- The user interface during modeling is provided using a [Connector template](/components/connectors/custom-built-connectors/connector-templates.md).

In a [Self-Managed](/self-managed/about-self-managed.md) environment, you manage the execution environment for Connectors yourself.
Using our [Connector runtime environments](/components/connectors/custom-built-connectors/connector-sdk.md#runtime-environments), you can consume any set of Connectors,
including the [out-of-the-box Connectors](/components/connectors/out-of-the-box-connectors/available-connectors-overview.md) and custom Connectors developed using the **[Connector SDK](/components/connectors/custom-built-connectors/connector-sdk.md)** and [Connector templates](/components/connectors/custom-built-connectors/connector-templates.md).

You can find a list of Connectors developed by Camunda, Partners, and the community in our
[Camunda Connectors Awesome List](https://github.com/camunda-community-hub/camunda-8-connectors#readme).

:::note
Some out-of-the-box Connectors are licensed under the [Camunda Self-Managed Free Edition license](https://camunda.com/legal/terms/cloud-terms-and-conditions/camunda-cloud-self-managed-free-edition-terms/).
:::

## Connector runtime and function

The Connector runtime environment can be installed using the supported [deployment options](/self-managed/platform-deployment/overview.md#deployment-options).

Currently, we support an installation of Connectors with [Docker](/self-managed/platform-deployment/docker.md#connectors),
[Docker Compose](/self-managed/platform-deployment/docker.md#docker-compose), [Helm charts](/self-managed/platform-deployment/helm-kubernetes/overview.md), and the [manual setup](/self-managed/platform-deployment/manual.md#run-connectors).

:::note
Inbound Connectors require Operate to be deployed as part of your Camunda Self-Managed installation.
If you don't use Operate with your cluster, you can still use Outbound Connectors.
:::

## Connector templates

For the modeling interface, you need to [provide Connector templates](/components/connectors/custom-built-connectors/connector-templates.md#providing-and-using-connector-templates).

For the [out-of-the-box Connectors](/components/connectors/out-of-the-box-connectors/available-connectors-overview.md) provided by Camunda,
the Connectors Bundle project provides a set of all Connector templates related to one [release version](https://github.com/camunda/connectors-bundle/releases).
If you use the [Docker Compose](/self-managed/platform-deployment/docker.md#docker-compose) installation, you can thus fetch all Connector templates that match the versions of the Connectors used in the backend.

Alternatively, you can fetch the JSON templates from the respective Connector's releases at respective connectors folder in the [bundle repository](https://github.com/camunda/connectors-bundle)
at `connectors/{connector name}/element-templates`.

You can use the Connector templates as provided or modify them to your needs as described in our [Connector templates guide](/components/connectors/custom-built-connectors/connector-templates.md).

Check out our [Connectors Awesome List](https://github.com/camunda-community-hub/camunda-8-connectors/tree/main) to find more Connectors.
