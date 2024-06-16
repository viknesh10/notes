* Binary Large objects
* Types
	* Block
		* Store text and binary data upto 4.7TB. Made up of individually managed blocks of data
	* Append
		* Block blobs that are optimized for append operations. Works well for logging where data is constantly appended
	* Page
		* Store upto 8TB. Any part of the file can be accessed at any time - for example, a virtual hard drive