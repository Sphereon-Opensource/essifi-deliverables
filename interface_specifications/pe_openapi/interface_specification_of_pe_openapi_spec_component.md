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


## Documentation for Models

- [Constraints](./Models/Constraints.md)
- [Field](./Models/Field.md)
- [Filter](./Models/Filter.md)
- [Format](./Models/Format.md)
- [FormatJwt](./Models/FormatJwt.md)
- [FormatLdp](./Models/FormatLdp.md)
- [HolderSubject](./Models/HolderSubject.md)
- [InputDescriptor](./Models/InputDescriptor.md)
- [PresentationDefinition](./Models/PresentationDefinition.md)
- [PresentationDefinitionStatus](./Models/PresentationDefinitionStatus.md)
- [PresentationSubmission](./Models/PresentationSubmission.md)
- [Schema](./Models/Schema.md)
- [Statuses](./Models/Statuses.md)
- [SubmissionRequirement](./Models/SubmissionRequirement.md)
- [SubmissionRequirement1](./Models/SubmissionRequirement1.md)
