# Custom Models Generator

### Generation Profiles

* [TypeScript](#TypeScript)

### TypeScript

PE-API, which contains an OpenAPI 3 models generator for Presentation Exchange objects is a maven based project. To set it up locally for development, run the following commands.

```
cd '<workspace>'
git clone git@github.com:Sphereon-Opensource/pe-api.git
cd pe-api
```

The POM.xml maven file in the root of the project contains a profiles section which lists the configuration and target programming languages to create different models packages. The following is an example to generate the models in the `Typescript` language by selecting the `models-typescript` profile. The command will generate the models in the directory `<workspace>/pe-api/target/sdks/models/typescript`.

```
mvn install -P models-typescript
cd target/sdks/models/typescript
npm pack
```

Expected result is that a file `/target/sdks/models/typescript/sphereon-pe-models-M.m.p.tgz` is generated where `M.m.p` is the current version which can be installed in the consumer project like so:

```
cd my-pe-models-consumer-prj
npm install --save '<workspace>/pe-api/target/sdks/models/typescript/sphereon-pe-models-M.m.p.tgz'
```

Importing and using the model

```
import {JwtObject} from '@sphereon/pe-models'

var jwtObject : JwtObject = {
    alg : ['someAlgorithm']
};

console.log(jwtObject);
```


To generate models for other programming languages please see [Swagger-codegen](https://github.com/swagger-api/swagger-codegen). 

