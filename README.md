`standalone-request-logger` is a very simple application that only logs the requests it receives.

To deploy it as a Knative service:

```
kubectl apply -n your-namespace config/knative-service.yaml
```

To deploy it as a regular Kubernetes service:

```
kubectl apply -n your-namespace config/kubernetes-service.yaml
```

If you need to build:

```bash
## TODO DOCKER_HUB_USERNAME=<your username here>
DOCKER_HUB_USERNAME=aliok

docker build src -t docker.io/${DOCKER_HUB_USERNAME}/standalone-request-logger
docker push docker.io/${DOCKER_HUB_USERNAME}/standalone-request-logger
```
