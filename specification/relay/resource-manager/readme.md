# Relay

> see https://aka.ms/autorest

This is the AutoRest configuration file for Relay.



---
## Getting Started
To build the SDK for Relay, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the Relay API.

``` yaml
openapi-type: arm
tag: package-2017-04
```

### Suppression

``` yaml
directive:
  - suppress: R4007
    reason: DefaultErrorResponseSchema - we will be Implementing in new API version
```


### Tag: package-2017-04

These settings apply only when `--tag=package-2017-04` is specified on the command line.

``` yaml $(tag) == 'package-2017-04'
input-file:
- Microsoft.Relay/stable/2017-04-01/relay.json
```


### Tag: package-2016-07

These settings apply only when `--tag=package-2016-07` is specified on the command line.

``` yaml $(tag) == 'package-2016-07'
input-file:
- Microsoft.Relay/stable/2016-07-01/relay.json
```


### Tag: package-2018-01-preview

These settings apply only when `--tag=package-2018-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2018-01-preview'
input-file:
- Microsoft.Relay/preview/2018-01-01-preview/Namespaces-preview.json
- Microsoft.Relay/preview/2018-01-01-preview/NetworkRuleSets-preview.json
- Microsoft.Relay/preview/2018-01-01-preview/PrivateEndpointConnection-preview.json
- Microsoft.Relay/preview/2018-01-01-preview/PrivateLinkResources-preview.json
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
  - repo: azure-sdk-for-go-track2
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-node
  - repo: azure-sdk-for-ruby
    after_scripts:
      - bundle install && rake arm:regen_all_profiles['azure_mgmt_relay']
  - repo: azure-resource-manager-schemas
```


## C#

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.Relay
  output-folder: $(csharp-sdks-folder)/relay/Microsoft.Azure.Management.Relay/src/Generated
  clear-output-folder: true
```

## Go

See configuration in [readme.go.md](./readme.go.md)

## Java

These settings apply only when `--java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-libraries-for-java clone>`.

``` yaml $(java)
azure-arm: true
fluent: true
namespace: com.microsoft.azure.management.relay
license-header: MICROSOFT_MIT_NO_CODEGEN
payload-flattening-threshold: 1
output-folder: $(azure-libraries-for-java-folder)/azure-mgmt-relay
```

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-2016-07
  - tag: package-2017-04
```

### Tag: package-2016-07 and java

These settings apply only when `--tag=package-2016-07 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2016-07' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.relay.v2016_07_01
  output-folder: $(azure-libraries-for-java-folder)/sdk/relay/mgmt-v2016_07_01
regenerate-manager: true
generate-interface: true
```

### Tag: package-2017-04 and java

These settings apply only when `--tag=package-2017-04 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2017-04' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.relay.v2017_04_01
  output-folder: $(azure-libraries-for-java-folder)/sdk/relay/mgmt-v2017_04_01
regenerate-manager: true
generate-interface: true
```





