# 

### RESTful App

For the REST-ful application run 

```
DOCKER_BUILDKIT=1 docker-compose up app
```

and access the api under `http://localhost:8000/docs`. In the test folder 
you find some images to play with.


## Development

For local development you have to take care about the following things.

### Python Environment
Install and activate a python environment, e.g. using poetry like

```
poetry install
poetry shell
```

Of course, you can use the dockerized interpreter too. When using an 
interpreter be careful to choose the top level directory as working directory.


### Run FastAPI


```
PYTHONPATH="." python src/run.py
```

### Update FastAPI using OpenAPI
When you want to update the API using the OpenAPI specification use this 
command:

```
fastapi-codegen --input oas/openapi.yaml -t jinja --output src
```