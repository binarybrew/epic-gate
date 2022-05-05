# Welcome to EPIC - the Application Gateway for Kubernetes

EPIC is a Gateway for Kubernetes. It uses the new gateway API to simplify the administration and creation of API and Application Gateways. The Gateway, EPIC, works with the EPIC Gateway Controller installed on the k8s cluster.

It simplifies the provisioning of API gateways, simply install the controller and create a gateway. No need to add an Ingress controller and a Load Balancer, and configure all of the components in-between. EPIC creates a gateway, connects it to the Internet, updates DNS records and then forward requests directly to the PODs hosting the applications.

This repo contains the installation yaml, Gateway Controller containers and configuration samples. 

The installation yaml is in the Package Registry, the containers are in the Container Registry

***These configuration samples are preconfigured for  the EPIC uswest region***

## Documentation

The [EPIC Kubernetes Application Gateway Documentation](https://www.epick8sgw.io/) is the best place to learn about the Gateway and get started.

## EPIC Gateway Service Manager
EPIC is a Application and API Gateway as a Service.  The Gateway Service Manager provide service configuration.  Login with your Github account and you can start a free trial of EPIC.

[EPIC Gateway Service Manager](https://gwsm.acnodal.io)

## Samples
These configuration samples are used in conjunction with the [Getting Started Guide](https://www.epick8sgw.io/docs/getting-started/).  In addition to installing and configuring a Gateway, the guide also includes a sample EchoServer application developed by Anodal (in javascript) that displays header, Cluster, Service and Gateway information.  Configuration samples for the Echo Server are in the [Gitlab EchoServer Repo](https://gitlab.com/acnodal/epic-echoserver)


| Example | Description |
|---------|-------------|
| gatewayclassconfig.yaml | Contains the EPIC configuration information |
| gatewayclass.yaml| Bind the GatewayClassConfig and makes the Gateway available for use |
| gateway.yaml| Creates a Gateway based upon the referenced gatwayclass/gatewayclassconfig|
| httproute.yaml | Creates the route match and binds together Gateways and Services |



## Gateway Templates
Each gateway is created from a template contained in the user namespace.  When a new user is created default templates are loaded into the user namespace.  The default samples are located in gwp_templates


