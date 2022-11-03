## 🤔 What is Istio?

Quick answer - Open Source service mesh

Istio is an Open source Service mesh which is an modernized service networking layer that provides transparent way to flexibly and easily automate application network function. 

Istio also helps microservices communicate with each other. 

### Basics of Istio:

![Istio basics](https://cdn.thenewstack.io/media/2021/04/a8201c9a-image1.jpg)

The above diagram shows an istio plane installed and distributing the configuration to all the proxies and gateways. 

Istio also establishes an application aware load balancing. Application admins can also manipulate the behaviour of traffic in Istion using the declarive api. 


### How it works?

Istio has two components:
    - data plane 
    - Control plane

Data plane establishes the communication between services. Service mesh uses proxies to intercept all your network traffic, allowing several features based on your config.

Control plane takes your desired config, and view it services and programs the proxy. 


![istio](https://istio.io/latest/img/service-mesh.svg)

<br><br>

<b>Resources:</b>


docs: https://istio.io/latest/docs/

Solo.io certification: https://academy.solo.io/get-started-with-istio