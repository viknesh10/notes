* When something breaks, alert someone to fix it
* Notifications in response to unexpected events
	* VM unresponsive
	* VM using excessive CPU
	* Application latency over 500ms
* Components
	* Alert rule
		* Monitored resource
		* Monitored telemetry
		* Conditions to trigger alert
		* Assigned severity
	* Action group
		* Action(s) taken when rule is triggered
		* Notification targets
			* Email/SMS to support personnel
			* Send to automation workflows
* In all scenarios, when something is not working as expected, Azure Monitor alerts inform the right group to do something about it