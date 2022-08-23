# http rest client plugin

## notes
- This provides a basic structure to play around with http requests around the provided mock.
- All files with the `*.http` ending are recognized as input files for the  [vscode-restclient plugin](https://github.com/Huachao/vscode-restclient).
- This example uses the `openapi-secured` OpenAPI definition of this project.

To run http client requests agains a real mock instance, execute from the root dir:
```
docker run --rm -ti -p 8080:8080 -v $PWD/openapi-secured:/opt/imposter/config outofcoffee/imposter-openapi
```

## usage
- Define all your vars used in your requests in `.vscode/settings.json`.
- Take care to NOT commit any secrets in public accessible repositories and/or within your regular code base.
- So it takes a careful decision to version the `.vscode/settings.json` file or not.

Example  of `.vscode/settings.json`:
```
{
    "rest-client.environmentVariables": {
        "dev": {
            "env": "dev",
            "basicAuth": "s3cr3t"
        },
        "test": {
            "env": "test",
            "basicAuth": "s3cr3t"
        },
        "prod": {
            "env": "prod",
            "basicAuth": "s3cr3t"
        },
    }
}
```

Each var like `env` or `basicAuth` can be used by opening a `.http` file and selecting one of the environments `dev`, `test`, `prod` in the VSCode status bar.

Example of usage in http file:
```
GET http://localhost:8080/{{env}}/api/pets
X-Custom-Api-Key: {{X-Custom-Api-Key}}
```

## advantages
- As all requests/responses can be saved as text files, so versioning and distribution is very simple.

## authentication notes

### basic auth
- base64(username:secret)

### another auth method
- ...
  
## Sources
- https://github.com/Huachao/vscode-restclient