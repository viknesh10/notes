* A computer or server that you have access to, exclusively
* Its virtual as it does not have its own exclusive hardware
* VMs are an [[Infrastructure-as-a-Service (IaaS)]] offering from Azure - manage everything else except hardware
* User Azure tools to manage a large number of VMs and even hybrid clouds
* Use Azure blueprints to make your VMs comply with company guidelines
* Azure will recommend improvements to ensure better security, higher availability and greater performance
* Choose amount of RAM, number of CPU's, as well as Operating Systems (Windows or Linux)
* Pro's
	* Control
		* Use VMs when you need to control all aspects of an environment or machine
	* Application
		* Install specific applications on your VMs
	* Existing Infrastructure
		* You can move move existing infrastructure to Azure - from on-premises or another cloud provider
* Con's
	* Not for everything
		* If you can use another Azure Service instead, its often worth it (lesser price)
	* Maintenance
		* A lot of maintenance with VMs or updates, patches and security concerns

## Scale sets
* A group of identical, load balanded VMs
* Benefits
	* Multiple VMs
		* Simple to manage multiple identical VMs using a load balancer
	* High availability
		* If one VM fails or stops, the others in the scale set step up and keep working
	* Auto scaling
		* Automatically match demand by adding or removing VMs from the scale set
	* Large scale
		* Run upto 1000 VMs in a single scale set
	* No extra cost
		* No added costs for using scale sets
## Spot VMs
* Save money by using unused capacity
* Can be evicted anytime
* Use for interruptible non-critical workloads
* Use with Scale sets
* Set a max price for the Spot VM