# imposter-playground
simple playground for imposter mock

## Run REST plugin with docker
```
docker run --rm -ti -p 8080:8080 -v $PWD/rest:/opt/imposter/config outofcoffee/imposter-rest
```

## Run OPENAPI plugin with docker
```
docker run --rm -ti -p 8080:8080 -v $PWD/openapi:/opt/imposter/config outofcoffee/imposter-openapi
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

## Sources
- https://docs.imposter.sh/getting_started/
- https://github.com/outofcoffee/imposter/tree/main/examples/soap/simple
- https://raw.githubusercontent.com/OAI/OpenAPI-Specification/main/examples/v3.0/callback-example.json