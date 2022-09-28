[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Lifecycle:Stable](https://img.shields.io/badge/Lifecycle-Maturing-007EC6)](https://github.com/bcgov/repomountie/blob/master/doc/lifecycle-badges.md)

# The Aries Endorser Configurations

This repository contains the [openshift-developer-tools](https://github.com/BCDevOps/openshift-developer-tools/tree/master/bin) compatible OpenShift configurations for the Aries Endorser Service. For more information, see the Aries Endorser Service repository [here](https://github.com/bcgov/aries-endorser-service)

For information on how to use these configurations with the `openshift-developer-tools scripts` please refer to the documentation; [README.md](https://github.com/BCDevOps/openshift-developer-tools/blob/master/bin/README.md).

## Endorser Services

```mermaid
classDiagram
	aries_endorser_proxy --> aries_endorser_agent : admin api
	aries_endorser_proxy --> aries_endorser_agent : http and ws ports
	aries_endorser_agent --> aries_endorser_wallet
	aries_endorser_api --> aries_endorser_api_db
	aries_endorser_api --> aries_endorser_agent : agent admin api
	external_agent --> aries_endorser_proxy : agent http and ws ports
	endorser_ui_TBD --> aries_endorser_api : controller admin api
```

## Getting Help or Reporting an Issue

To report bugs/issues/feature requests, please file an [issue](../../issues).

## How to Contribute

If you would like to contribute, please see our [CONTRIBUTING](./CONTRIBUTING.md) guidelines.

Please note that this project is released with a [Contributor Code of Conduct](./CODE_OF_CONDUCT.md). 
By participating in this project you agree to abide by its terms.