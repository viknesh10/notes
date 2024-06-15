* Load balancer distributes new inbound flows that arrive on the Load balancer's frontend to backend pool instances, according to rules and health probes
* Inbound flows
	* Traffic from the internet or local network
* Frontend
	* The access point for the load balancer. All traffic goes here first
* Backend pool
	* The VM instances receiving traffic
* Rules and health probes
	* Checks to ensure backend instance can receive the data

## Scenarios
* Internet traffic
	* Balance the load of incoming internet traffic into a system or application
* Internal networks
	* A load balancer works well with internal applications
* Port forwarding
	* Traffic can be forwarded to a specific machine in the backend pool
* Outbound traffic
	* Allow outbound connectivity for backend pool VMs