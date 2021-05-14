# PE-OpenAPI Specification

The [DIF Presentation Exchange v1.0.0 specification](https://identity.foundation/presentation-exchange/) describe in detail the structure of the models required by verifier and holder of verifiable credentials. These specifications are implemented in the YAML files in the pe-openapi maven project.

In order to use these directly follow steps below:

Clone the git repo (or download zip) from github
```
cd '<workspace>'
git clone git@github.com:Sphereon-Opensource/pe-openapi.git
cd pe-openapi
```

The `swagger` folder holds the YAMLs these can be processed using swagger-codegen or openapi-codegen plugins to generate the desired code.