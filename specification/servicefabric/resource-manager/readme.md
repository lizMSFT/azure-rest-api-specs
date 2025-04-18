# ServiceFabric

> see https://aka.ms/autorest

This is the AutoRest configuration file for Service Fabric.



---
## Getting Started
To build the SDK for ServiceFabricManagementClient, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the ServiceFabricManagementClient API.

``` yaml
title: ServiceFabricManagementClient
description: Service Fabric Management Client
openapi-type: arm
tag: package-2021-06

directive:
  - suppress: ListInOperationName
    reason: Modifying the operation names would break the backwards compatibility of the API.
  - suppress: LongRunningResponseStatusCode
    reason: The validation tools do not properly recognize 202 as a supported response code.
  - suppress: SummaryAndDescriptionMustNotBeSame
    reason: There are a lot of APIs with missing summary content. While it is being worked on disabling this to ensure that we catch and fix other violations.
  - suppress: TrackedResourceListByImmediateParent
    reason: Proxy resources are not properly evaluated by the validation toolset.
  - suppress: DefinitionsPropertiesNamesCamelCase
    reason: Modifying the operation names would break the backwards compatibility of the API.
  - suppress: EnumInsteadOfBoolean
    reason: The boolean properties are actually boolean value in the Service Fabric's application model.
  - suppress: TrackedResourceGetOperation
    reason: Proxy resources are not properly evaluated by the validation toolset.
  - suppress: TrackedResourcePatchOperation
    reason: Proxy resources are not properly evaluated by the validation toolset.
  - suppress: TrackedResourceListByResourceGroup
    reason: Proxy resources are not properly evaluated by the validation toolset.
  - suppress: TrackedResourceListBySubscription
    reason: Proxy resources are not properly evaluated by the validation toolset.
  - suppress: DescriptionAndTitleMissing
    reason: There are a lot of APIs with missing titles. While it is being worked on disabling this to ensure that we catch and fix other violations.
  - suppress: Example Validations
    reason: There are open issues (bugs) in the validator affecting some of the examples and since there is no way to selectively disable the validation for a particular example or paths, all of the example validation is being turned off.
  - suppress: Example Validations
    reason: There are open issues (bugs) in the validator affecting some of the examples and since there is no way to selectively disable the validation for a particular example or paths, all of the example validation is being turned off.
```

### Tag: package-2023-11-preview

These settings apply only when `--tag=package-2023-11-preview` is specified on the command line.

``` yaml $(tag) == 'package-2023-11-preview'
input-file:
- Microsoft.ServiceFabric/preview/2023-11-01-preview/cluster.json
- Microsoft.ServiceFabric/preview/2023-11-01-preview/application.json
```

### Tag: package-2021-06

These settings apply only when `--tag=package-2021-06` is specified on the command line.

``` yaml $(tag) == 'package-2021-06'
input-file:
- Microsoft.ServiceFabric/stable/2021-06-01/cluster.json
- Microsoft.ServiceFabric/stable/2021-06-01/application.json
```

### Tag: package-2020-03

These settings apply only when `--tag=package-2020-03` is specified on the command line.

``` yaml $(tag) == 'package-2020-03'
input-file:
- Microsoft.ServiceFabric/stable/2020-03-01/cluster.json
- Microsoft.ServiceFabric/stable/2020-03-01/application.json
```

### Tag: package-2020-12-preview

These settings apply only when `--tag=package-2020-12-preview` is specified on the command line.

``` yaml $(tag) == 'package-2020-12-preview'
input-file:
- Microsoft.ServiceFabric/preview/2020-12-01-preview/cluster.json
- Microsoft.ServiceFabric/preview/2020-12-01-preview/application.json
```

### Tag: package-2020-01-preview

These settings apply only when `--tag=package-2020-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2020-01-preview'
input-file:
- Microsoft.ServiceFabric/preview/2020-01-01-preview/managedcluster.json
- Microsoft.ServiceFabric/preview/2020-01-01-preview/nodetype.json
```

### Tag: package-2019-11-preview

These settings apply only when `--tag=package-2019-11-preview` is specified on the command line.

``` yaml $(tag) == 'package-2019-11-preview'
input-file:
- Microsoft.ServiceFabric/preview/2019-11-01-preview/cluster.json
- Microsoft.ServiceFabric/preview/2019-11-01-preview/application.json
```

### Tag: package-2019-06-preview

These settings apply only when `--tag=package-2019-06-preview` is specified on the command line.

``` yaml $(tag) == 'package-2019-06-preview'
input-file:
- Microsoft.ServiceFabric/preview/2019-06-01-preview/cluster.json
- Microsoft.ServiceFabric/preview/2019-06-01-preview/application.json
```

### Tag: package-2019-03

These settings apply only when `--tag=package-2019-03` is specified on the command line.

``` yaml $(tag) == 'package-2019-03'
input-file:
- Microsoft.ServiceFabric/stable/2019-03-01/cluster.json
- Microsoft.ServiceFabric/stable/2019-03-01/application.json
```

### Tag: package-2019-03-preview

These settings apply only when `--tag=package-2019-03-preview` is specified on the command line.

``` yaml $(tag) == 'package-2019-03-preview'
input-file:
- Microsoft.ServiceFabric/preview/2019-03-01-preview/cluster.json
- Microsoft.ServiceFabric/preview/2019-03-01-preview/application.json
```

### Tag: package-2018-02

These settings apply only when `--tag=package-2018-02` is specified on the command line.

``` yaml $(tag) == 'package-2018-02'
input-file:
- Microsoft.ServiceFabric/stable/2018-02-01/cluster.json
- Microsoft.ServiceFabric/preview/2017-07-01-preview/application.json
```

### Tag: package-2017-07

These settings apply only when `--tag=package-2017-07` is specified on the command line.

``` yaml $(tag) == 'package-2017-07'
input-file:
- Microsoft.ServiceFabric/preview/2017-07-01-preview/servicefabric.json
```

### Tag: package-2016-09

These settings apply only when `--tag=package-2016-09` is specified on the command line.

``` yaml $(tag) == 'package-2016-09'
input-file:
- Microsoft.ServiceFabric/stable/2016-09-01/servicefabric.json
```

### Tag: package-2018-02-only

These settings apply only when `--tag=package-2018-02-only` is specified on the command line.

``` yaml $(tag) == 'package-2018-02-only'
input-file:
- Microsoft.ServiceFabric/stable/2018-02-01/cluster.json
```

---
# Code Generation


## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-net
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-node
  - repo: azure-sdk-for-ruby
    after_scripts:
      - bundle install && rake arm:regen_all_profiles['azure_mgmt_service_fabric']
  - repo: azure-resource-manager-schemas
  - repo: azure-powershell
```


## Go

See configuration in [readme.go.md](./readme.go.md)

## Python

See configuration in [readme.python.md](./readme.python.md)

## Java

See configuration in [readme.java.md](./readme.java.md)



