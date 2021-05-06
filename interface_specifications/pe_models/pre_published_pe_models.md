# Using Pre-published Models

Pre-published models can be used in desired project from various sources. For example 'TypeScript' models can be used from [NPMJS @sphereon/pe-models](https://www.npmjs.com/package/@sphereon/pe-models).

### Published Models

* [TypeScript](#TypeScript)


### TypeScript

This is an example where you create a new `NPM` project, import and use `JwtObject` model from a pre-published `node-module`. Similarly, you can import and use other models.

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
