# blue-service Project

This project aims to be discovered by Stork Kubernetes Service Discovery Quickstart.
This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .


## Packaging the application and building and push a container image

The application can be packaged using the following command, with the quarkus.container-image.build=true and quarkus.container-image.push=true, it will build and push a container image. Chek the configuration in the `application.properties` file.

```shell script
./mvnw clean package -Dquarkus.container-image.build=true -Dquarkus.container-image.push=true
```
Two files named kubernetes.json and kubernetes.yml have been generated under the target/kubernetes/ directory.

The generated manifest can be applied to the cluster from the project root using kubectl:

```shell
kubectl apply -f target/kubernetes/kubernetes.yml
```

Now, you should be able to access the blue service in a browser. Navigate to http://blue-service.127.0.0.1.nip.io/blue


## Related Guides

- Kubernetes ([guide](https://quarkus.io/guides/kubernetes)): Generate Kubernetes resources from annotations
- RESTEasy JAX-RS ([guide](https://quarkus.io/guides/rest-json)): REST endpoint framework implementing JAX-RS and more

## Provided Code

### RESTEasy JAX-RS

Easily start your RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)


