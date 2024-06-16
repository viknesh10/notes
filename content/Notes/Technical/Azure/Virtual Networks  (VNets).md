* Fundamental part of Azure infrastructure
* Address space
	* A range of IP addresses you can use for your resources
## Cloud advantages
* Scaling
	* Adding more VNets or more addresses to one is simple
* High availability
	* Peering VNets, using a load balancer, or using a VPN gateway all increase availability
* Isolation
	* Manage and organise resources with subnets and network security groups

## Peering
* Lets you connect two or more VNets on Azure
* Always uses Azure's backbone network and never through public internet
* Benefits
	* Low latency, high bandwidth
	* Link Separate networks
	* Data transfer
		* Transfer data easily between subscriptions and deployment models in separate regions