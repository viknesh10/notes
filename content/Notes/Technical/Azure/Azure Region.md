* A region is a set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network

## Choosing a region
* Location
	* Choose a region closest to your users to minimize latency
* Features
	* Some features arent in all regions.
	* If you need a specific feature, some regions may be unavailable
* Price
	* The price of services vary from region to region

## Paired region
* Each region is paired
	* Paired within the same geographical zone except Brazil South which is paired to South Central US
* Outage failover
	* If the primary region has an outage, you can failover to the secondary region
* Planned updates
	* Only one region in a pair is updated at any one time
* Replication
	* Some services used pair regions for replication