## 🤔 What is Service Mesh?

If you are into Microservices or Kubernetes, most probably you might have heard the term Service mesh. But what is it???

<b> <i>Service mesh is an dedicated infrastructure layer which helps in facilitating the Service to Service communication between service/microservices.<i></b>

- It performs the service delivery to the other services, performs load balancing, service discovery.

### Why you need Service mesh?

Let's assume you have microservice A and microservice B, the communication between these two can be established very easily. But what if you have several microservices and you application is receiving heavy traffic, how can you manage the service disovery, and other communication related things. 

Service mesh installs an proxy instance in the service called sidecar proxy which will do the service discovery, traffic routing, authentication of the other services. This sidecar helps to identify the other services, helps in authenticate, access them, establish the communication between them. 

Using service mesh helps the devs to mainly focus on the application core development, and service mesh didn't introduce new functionality/code changes to the application. 






