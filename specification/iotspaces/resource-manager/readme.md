# IoTSpaces Service

> see https://aka.ms/autorest

This is the AutoRest configuration file for IoTSpaces Service.

---
## Getting Started
To build the SDK for IoTSpaces Service, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the IoTSpaces Service.

``` yaml
openapi-type: arm
tag: package-2017-10-preview
```


### Tag: package-2017-10-preview

These settings apply only when `--tag=package-2017-10-preview` is specified on the command line.

``` yaml $(tag) == 'package-2017-10-preview'
input-file: 
- Microsoft.IoTSpaces/preview/2017-10-01-preview/iotspaces.json
```

---
# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-go
```

## CSharp Settings

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.IoTSpaces
  payload-flattening-threshold: 1
  output-folder: $(csharp-sdks-folder)/IoTSpaces/Management.IoTSpaces/Generated
  clear-output-folder: true
```

## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  clear-output-folder: true
  namespace: iotspaces
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2017-10-preview
```

### Tag: package-2017-10-preview and go

These settings apply only when `--tag=package-2017-10-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2017-10-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2017-10-01-preview/$(namespace)
```
