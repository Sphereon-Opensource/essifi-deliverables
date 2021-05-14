# Using Pre-published PE-Models

Pre-published models can be used in your desired project from various sources. For example 'TypeScript' models can be used from [NPMJS @sphereon/pe-models](https://www.npmjs.com/package/@sphereon/pe-models). These are simple typescript model interfaces with fields defined in them. One can import and use them. A more elaborate sequence of steps is described in the [PE-OpenAPI Models Generator](./interface_specification_of_pe_openapi_models_generator_component.md)


### Published Models and languages

* [TypeScript](#TypeScript)


### TypeScript

This is an example where you create a new `NPM` project, import and use the `JwtObject` pe-model from a pre-published `node-module`. Similarly, you can import and use other models.

```
cd '<workspace>'
mkdir my-pe-models-consumer-prj
cd my-pe-models-consumer-prj
npm init
```

Pre-built models can be installed directly from npmjs.com with following commands

```
npm install
npm install --save @sphereon/pe-models
```

Importing and using the model

```
import {JwtObject} from '@sphereon/pe-models'

var jwtObject : JwtObject = {
    alg : ['someAlgorithm']
};

console.log(jwtObject);
```
