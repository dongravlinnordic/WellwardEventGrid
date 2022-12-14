## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go) && !$(track2)
go:
  license-header: MICROSOFT_MIT_NO_VERSION
  clear-output-folder: true
  namespace: managementgroups
```

``` yaml $(go) && $(track2)
license-header: MICROSOFT_MIT_NO_VERSION
module-name: sdk/resourcemanager/managementgroups/armmanagementgroups
module: github.com/Azure/azure-sdk-for-go/$(module-name)
output-folder: $(go-sdk-folder)/$(module-name)
azure-arm: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2021-04
  - tag: package-2020-10
  - tag: package-2020-05
  - tag: package-2020-02
  - tag: package-2019-11
  - tag: package-2018-03
  - tag: package-2018-01
  - tag: package-2017-11
  - tag: package-2017-08
```
### Tag: package-2021-04 and go

These settings apply only when `--tag=package-2021-04 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2021-04' && $(go)
output-folder: $(go-sdk-folder)/services/resources/mgmt/2021-04-01/$(namespace)
```

### Tag: package-2020-10 and go

These settings apply only when `--tag=package-2020-10 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2020-10' && $(go)
output-folder: $(go-sdk-folder)/services/resources/mgmt/2020-10-01/$(namespace)
```

### Tag: package-2020-05 and go

These settings apply only when `--tag=package-2020-05 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2020-05' && $(go)
output-folder: $(go-sdk-folder)/services/resources/mgmt/2020-05-01/$(namespace)
```

### Tag: package-2020-02 and go

These settings apply only when `--tag=package-2020-02 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2020-02' && $(go)
output-folder: $(go-sdk-folder)/services/resources/mgmt/2020-02-01/$(namespace)
```

### Tag: package-2019-11 and go

These settings apply only when `--tag=package-2019-11 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2019-11' && $(go)
output-folder: $(go-sdk-folder)/services/resources/mgmt/2019-11-01/$(namespace)
```

### Tag: package-2018-03 and go

These settings apply only when `--tag=package-2018-03 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2018-03' && $(go)
output-folder: $(go-sdk-folder)/services/preview/resources/mgmt/2018-03-01-preview/$(namespace)
```

### Tag: package-2018-01 and go

These settings apply only when `--tag=package-2018-01 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2018-01' && $(go)
output-folder: $(go-sdk-folder)/services/preview/resources/mgmt/2018-01-01-preview/$(namespace)
```

### Tag: package-2017-11 and go

These settings apply only when `--tag=package-2017-11 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2017-11' && $(go)
output-folder: $(go-sdk-folder)/services/preview/resources/mgmt/2017-11-01-preview/$(namespace)
```

### Tag: package-2017-08 and go

These settings apply only when `--tag=package-2017-08 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag)=='package-2017-08' && $(go)
output-folder: $(go-sdk-folder)/services/preview/resources/mgmt/2017-08-31-preview/$(namespace)
```
