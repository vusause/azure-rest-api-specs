# MySql

> see https://aka.ms/autorest

This is the AutoRest configuration file for MySql.

---

## Getting Started

To build the SDK for MySql, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`

---

## Configuration

### Basic Information

These are the global settings for the MySql API.

``` yaml
title: MySQLManagementClient
description: The Microsoft Azure management API provides create, read, update, and delete functionality for Azure MySQL resources including servers, databases, firewall rules, VNET rules, log files and configurations with new business model.
openapi-type: arm
tag: package-2020-01-01
```

``` yaml $(package-flexibleservers)
tag: package-flexibleserver-2021-12-01-preview
```

``` yaml $(package-singleservers)
tag: package-2020-01-01
```

### Tag: package-2017-12-01-preview

These settings apply only when `--tag=package-2017-12-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2017-12-01-preview'
input-file:
- Microsoft.DBforMySQL/preview/2017-12-01-preview/mysql.json
```

### Tag: package-2017-12-01

These settings apply only when `--tag=package-2017-12-01` is specified on the command line.

``` yaml $(tag) == 'package-2017-12-01'
input-file:
- Microsoft.DBforMySQL/stable/2017-12-01/mysql.json
- Microsoft.DBforMySQL/stable/2017-12-01/ServerSecurityAlertPolicies.json
```

### Tag: package-2018-06-01-privatepreview

These settings apply only when `--tag=package-2018-06-01-privatepreview` is specified on the command line.

``` yaml $(tag) == 'package-2018-06-01-privatepreview'
input-file:
- Microsoft.DBforMySQL/preview/2018-06-01-privatepreview/mysql.json
- Microsoft.DBforMySQL/preview/2018-06-01-privatepreview/PrivateEndpointConnections.json
- Microsoft.DBforMySQL/preview/2018-06-01-privatepreview/PrivateLinkResources.json
```

### Tag: package-2018-06-01

These settings apply only when `--tag=package-2018-06-01` is specified on the command line.

``` yaml $(tag) == 'package-2018-06-01'
input-file:
- Microsoft.DBforMySQL/stable/2017-12-01/mysql.json
- Microsoft.DBforMySQL/stable/2017-12-01/ServerSecurityAlertPolicies.json
- Microsoft.DBforMySQL/stable/2018-06-01/QueryPerformanceInsights.json
- Microsoft.DBforMySQL/stable/2018-06-01/PerformanceRecommendations.json
- Microsoft.DBforMySQL/stable/2018-06-01/PrivateEndpointConnections.json
- Microsoft.DBforMySQL/stable/2018-06-01/PrivateLinkResources.json
```

### Tag: package-2020-01-01-privatepreview

These settings apply only when `--tag=package-2020-01-01-privatepreview` is specified on the command line.

``` yaml $(tag) == 'package-2020-01-01-privatepreview'
input-file:
- Microsoft.DBforMySQL/preview/2020-01-01-privatepreview/DataEncryptionKeys.json
```

### Tag: package-2020-01-01

These settings apply only when `--tag=package-2020-01-01` is specified on the command line.

``` yaml $(tag) == 'package-2020-01-01'
input-file:
- Microsoft.DBforMySQL/stable/2017-12-01/mysql.json
- Microsoft.DBforMySQL/stable/2017-12-01/ServerSecurityAlertPolicies.json
- Microsoft.DBforMySQL/stable/2018-06-01/QueryPerformanceInsights.json
- Microsoft.DBforMySQL/stable/2018-06-01/PerformanceRecommendations.json
- Microsoft.DBforMySQL/stable/2018-06-01/PrivateEndpointConnections.json
- Microsoft.DBforMySQL/stable/2018-06-01/PrivateLinkResources.json
- Microsoft.DBforMySQL/stable/2020-01-01/DataEncryptionKeys.json
- Microsoft.DBforMySQL/stable/2020-01-01/Servers.json
```

### Tag: package-2020-07-01-privatepreview

These settings apply only when `--tag=package-2020-07-01-privatepreview` is specified on the command line.

``` yaml $(tag) == 'package-2020-07-01-privatepreview'
input-file:
- Microsoft.DBforMySQL/preview/2020-07-01-privatepreview/mysql.json
```

### Tag: package-2020-07-01-preview

These settings apply only when `--tag=package-2020-07-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2020-07-01-preview'
input-file:
- Microsoft.DBforMySQL/preview/2020-07-01-preview/mysql.json
```

### Tag: package-flexibleserver-2021-05-01-preview

These settings apply only when `--tag=package-flexibleserver-2021-05-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2021-05-01-preview'
input-file:
- Microsoft.DBforMySQL/preview/2021-05-01-preview/mysql.json
```

### Tag: package-flexibleserver-2021-05-01

These settings apply only when `--tag=package-flexibleserver-2021-05-01` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2021-05-01'
input-file:
- Microsoft.DBforMySQL/stable/2021-05-01/mysql.json
```

### Tag: package-flexibleserver-2021-12-01-preview

These settings apply only when `--tag=package-flexibleserver-2021-12-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-flexibleserver-2021-12-01-preview'
input-file:
- Microsoft.DBforMySQL/preview/2021-12-01-preview/Backups.json
- Microsoft.DBforMySQL/preview/2021-12-01-preview/Configurations.json
- Microsoft.DBforMySQL/preview/2021-12-01-preview/Databases.json
- Microsoft.DBforMySQL/preview/2021-12-01-preview/FirewallRules.json
- Microsoft.DBforMySQL/preview/2021-12-01-preview/FlexibleServers.json
- Microsoft.DBforMySQL/preview/2021-12-01-preview/LogFiles.json
- Microsoft.DBforMySQL/preview/2021-12-01-preview/ServiceOperations.json
```

## Suppression

``` yaml
directive:
  - suppress: PathResourceProviderNamePascalCase
    reason: The name of the provider is Microsoft.DBforMySQL
  - suppress: OperationsApiResponseSchema
    from: mysql.json
    reason: Property isDataAction is not included in get operation reponse body
  - suppress: OperationsApiResponseSchema
    from: Microsoft.DBforMySQL/preview/2021-12-01-preview/ServiceOperations.json
    reason: Property isDataAction is not included in get operation reponse body
```

---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-net
  - repo: azure-sdk-for-python-track2
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-node
  - repo: azure-resource-manager-schemas
  - repo: azure-powershell
```

### C#

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.MySQL
  output-folder: $(csharp-sdks-folder)/mysql/Microsoft.Azure.Management.MySQL/src/mysql/Generated
  clear-output-folder: true
```

## Python

See configuration in [readme.python.md](./readme.python.md)

## Go

See configuration in [readme.go.md](./readme.go.md)

## Java

See configuration in [readme.java.md](./readme.java.md)
