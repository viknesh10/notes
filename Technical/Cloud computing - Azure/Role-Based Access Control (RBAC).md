* Define user access
	* You can define specific user access to individual resources
* Minimum access
	* RBAC can enable minimum access necessary to resources
	* Ensures only users with valid access can manage resources
* Target Specific Use cases
	* Be very explicit about uses and access
	* Like, allow an application access to certain resources or allow a user to manage resources in a resource group
* Role assignment
	* Three elements
		* Security Principal
			* An object representing an entity such as a user or group, which can access the resource
		* Role Definition
			* A collection of permissions like read, write and delete
		* Scope
			* The resources the access applies to.
			* Specify which role can access a resource or a resource group
* Locks
	* Assigning
		* Assign a lock to a subscription, resource group or resource
	* Types
		* Delete
			* Cant delete the locked object
		* Read-Only
			* Cant make any changes to the object
	* Locked means locked
		* A lock needs to be removed before the locked actions can be performed again