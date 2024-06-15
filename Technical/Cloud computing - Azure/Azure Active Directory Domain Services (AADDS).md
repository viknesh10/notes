* A managed service
* Create unique namespace/domain name
	* Standalone domain and not an extension of on-premises AD Domain
* One-way sync from [[Azure Active Directory (AAD)]] to AADDS
	* Sync users, groups and credentials
	* AAD may also bidirectionally sync with on-premises AD
## Scenario
* To lift and shift legacy applications to Azure VMs
	* Application does not support modern authentication
* To integrate application with classic, cloud-hosted AD using managed services
* In this case, solution is to have a cloud-hosted legacy application that authenticates with AADDDS