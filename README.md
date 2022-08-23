# imposter-playground
simple playground for [imposter mock](https://docs.imposter.sh) and [vscode-rest client](https://github.com/Huachao/vscode-restclient).

## motivation
- Distributed teams are often confronted with the situation to agree on an shared API.
- For http based API's the [OpenAPI](https://swagger.io/docs/specification/about/) standard is a excellent starting point.
- This repo provides a template to define the api inside the [imposter mock](https://docs.imposter.sh) and also to consume via the [vscode-rest client](https://github.com/Huachao/vscode-restclient). 

## Run REST plugin with docker
```
docker run --rm -ti -p 8080:8080 -v $PWD/rest:/opt/imposter/config outofcoffee/imposter-rest
```

## Run OPENAPI plugin with docker
```
docker run --rm -ti -p 8080:8080 -v $PWD/openapi:/opt/imposter/config outofcoffee/imposter-openapi
```

## Run OPENAPI plugin with docker (secured)
```
docker run --rm -ti -p 8080:8080 -v $PWD/openapi-secured:/opt/imposter/config outofcoffee/imposter-openapi
```

## Run OPENAPI plugin with docker using static named payload
```
docker run --rm -ti -p 8080:8080 -v $PWD/static-named-example:/opt/imposter/config outofcoffee/imposter-openapi
```

## Run OPENAPI plugin with docker using scripted named payload
```
docker run --rm -ti -p 8080:8080 -v $PWD/scripted-named-example:/opt/imposter/config outofcoffee/imposter-openapi
```

## Run SOAP plugin with docker
```
docker run --rm -ti -p 8080:8080 -v $PWD/soap:/opt/imposter/config outofcoffee/imposter-all
```

## VSCode REST Client
Details inside `./http/README.md`.

## Sources
- https://docs.imposter.sh/getting_started/
- https://github.com/outofcoffee/imposter/tree/main/examples/soap/simple
- https://raw.githubusercontent.com/OAI/OpenAPI-Specification/main/examples/v3.0/callback-example.json
- https://marketplace.visualstudio.com/items?itemName=humao.rest-client
- https://github.com/Huachao/vscode-restclient
- https://docs.imposter.sh/security/#authentication