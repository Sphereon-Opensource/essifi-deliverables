# Custom Models Generator

### Generation Profiles

* [TypeScript](#TypeScript)

### TypeScript

Models generator(i.e. pe-api) is a maven based project. To set it up locally for development, run following commands.

```
cd '<workspace>'
git clone git@github.com:Sphereon-Opensource/pe-api.git
cd pe-api
```

POM file in the root of the project contains profiles section which lists the configuration to create models. Following is an example to generate the models in `Typescript` language by selecting `models-typescript` profile. The command will generate the models in `<workspace>/pe-api/target/sdks/models/typescript`.

```
mvn install -P models-typescript
cd target/sdks/models/typescript
npm pack
```

Expected result is that a file `/target/sdks/models/typescript/sphereon-pe-models-M.m.p.tgz` is generated where `M.m.p` is arbitrary which can be installed in the consumer project like so:

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


To generate models for in other languages please see [Swagger-codegen](https://github.com/swagger-api/swagger-codegen). 

